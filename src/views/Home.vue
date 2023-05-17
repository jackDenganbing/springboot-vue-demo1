<template>
  <div class="home">
  </div>
</template>

<script>

export default {
  data() {
    return {
      url: service.defaults.baseURL + "aaa/bbb", // 这里写上传文件的地址
      form: {
        ipArea: "",
        sourceMachineIp: ""
      }
    };
  },
  computed: {
    // 这里定义上传文件时携带的参数，即表单数据
    upData: function () {
      return {
        body: this.form
      }
    }
  },
  methods: {
    add(form) {
      this.$refs[form].validate(async valid => {
        if (valid) {
          // 表单验证通过后使用组件自带的方法触发上传事件
          this.$refs.upload.submit()
        } else {
          return false;
        }
      });
    },
    // 成功上传文件
    upFile(res, file) {
      if (res.status == 200) {
        // 文件上传成功后的回调，比如一些提示信息或者页面跳转都写在这里
        this.$message.success(res.info);
      } else {
        this.$message.warning(res.info);
        let _this = this;
        setTimeout(function () {
          _this.$refs.upload.clearFiles();
        }, 1000);
      }
    },
    // 上传文件超出个数
    handleExceed(files, fileList) {
      this.$message.warning(`当前只能选择上传2 个证书`);
    },
    //  移除文件
    handleRemove(res, file, fileList) {
      this.$message.warning(`移除当前${res.name}证书，请重新选择证书上传！`);
    }
  }
}
</script>
