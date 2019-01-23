<template>
  <div id="editor">

    <quill-editor ref="textEditor"
                  v-model="content"
                  :options="editorOption">
      <!--<div id="toolbar" slot="toolbar">
        <input type="file" id="pickFiles" />
        <button id="custom-button" @click="test" title="视频"><i class="iconfont el-icon-circle-plus"></i></button>
      </div>-->
      <!-- 文件上传input 将它隐藏-->
      <div slot="toolbar">
        <el-upload class="upload-demo" :action="qnLocation" :before-upload='beforeUpload' :data="uploadData" :on-success='upScuccess'
                   ref="upload" style="display:block"><i class="icon-video"></i>
          <!--<el-button size="small" type="primary" id="imgInput" element-loading-text="插入中,请稍候">点击上传</el-button>-->
        </el-upload>
      </div>

    </quill-editor>
  </div>
</template>

<script>
  import * as Quill from 'quill'  //引入编辑器
  //quill编辑器的字体
  var fonts = ['SimSun', 'SimHei','Microsoft-YaHei','KaiTi','FangSong','Arial','Times-New-Roman','sans-serif'];
  var Font = Quill.import('formats/font');
  Font.whitelist = fonts; //将字体加入到白名单
  Quill.register(Font, true);
    export default {
      name: "Editor",
      data(){
        return{
          content:'',
          editorOption: {
            modules: {
              toolbar: [
                ['bold', 'italic', 'underline', 'strike'],        //加粗，斜体，下划线，删除线
                ['blockquote', 'code-block'],         //引用，代码块


                [{'header': 1}, {'header': 2}],               // 标题，键值对的形式；1、2表示字体大小
                [{'list': 'ordered'}, {'list': 'bullet'}],          //列表
                [{'script': 'sub'}, {'script': 'super'}],      // 上下标
                [{'indent': '-1'}, {'indent': '+1'}],          // 缩进
                [{'direction': 'rtl'}],                         // 文本方向


                [{'size': ['small', false, 'large', 'huge']}],  // 字体大小
                [{'header': [1, 2, 3, 4, 5, 6, false]}],         //几级标题


                [{'color': []}, {'background': []}],          // 字体颜色，字体背景颜色
                [{'font': []}],         //字体
                [{'align': []}],        //对齐方式


                ['clean'],        //清除字体样式
                ['image']        //上传图片、上传视频

              ]
            },
            theme: 'snow'
          }
        }
      },
      methods:{

      }
    }
</script>

<style scoped>
  .quill-editor{
    height: 500px;
    width: 900px;
    margin: 0 auto;
    position: relative;
  }
  .upload-demo{
    position: absolute;
    top: 36px;
    left: 580px;
  }
/*  #pickFiles{
    width: 26px;
    height: 18px;
    position: absolute;
    top: 36px;
    right: 330px;
    z-index: 9999;

  !*  display: none;*!
  }
  #custom-button{
    position: absolute;
    top: 36px;
    right: 326px;
    cursor: pointer;
    background: transparent;
    color: transparent;
    border: none;
  }*/
</style>
