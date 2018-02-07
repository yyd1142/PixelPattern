<template>
  <div class="hello">
    <!-- h:17 w:13 -->
    <ul class="page-wrap" :style="{ height: `${cellPx}px` }" v-for="i, index in 17">
      <li :id="`p${index}_${subIndex}`" class="item" :style="{ width: `${cellPx}px`, height: `${cellPx}px` }" v-for="j, subIndex in 13"></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      clientWidth: 0,
      cellPx: 0,
      blackColor: '#000000',
      redColor: '#db6a66',
      huiColor: '#998f8d',
      rubaiColor: '#f1e8d7'
    }
  },
  mounted() {
    this.$nextTick(() => {
      this.clientWidth = document.body.clientWidth
      this.cellPx = this.clientWidth / 13
      this.setPhoto()
    })
  },
  methods: {
    setPhoto(){
      document.getElementById(`p${0}_${4}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${0}_${5}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${0}_${7}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${0}_${8}`).style.backgroundColor = this.blackColor;

      document.getElementById(`p${1}_${3}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${1}_${4}`).style.backgroundColor = this.redColor;
      document.getElementById(`p${1}_${5}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${1}_${7}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${1}_${8}`).style.backgroundColor = this.redColor;
      document.getElementById(`p${1}_${9}`).style.backgroundColor = this.blackColor;

      for(let i = 0; i < 4; i++) {
        let x = i + 2;
        document.getElementById(`p${x}_${2}`).style.backgroundColor = this.blackColor;
        document.getElementById(`p${x}_${3}`).style.backgroundColor = this.redColor;
        document.getElementById(`p${x}_${4}`).style.backgroundColor = this.redColor;
        document.getElementById(`p${x}_${5}`).style.backgroundColor = this.blackColor;
        document.getElementById(`p${x}_${7}`).style.backgroundColor = this.blackColor;
        document.getElementById(`p${x}_${8}`).style.backgroundColor = this.redColor;
        document.getElementById(`p${x}_${9}`).style.backgroundColor = this.redColor;
        document.getElementById(`p${x}_${10}`).style.backgroundColor = this.blackColor;
      }
      for(let i = 0; i < 2; i++) {
        let x = i + 6;
        document.getElementById(`p${x}_${2}`).style.backgroundColor = this.blackColor;
        document.getElementById(`p${x}_${3}`).style.backgroundColor = this.redColor;
        document.getElementById(`p${x}_${4}`).style.backgroundColor = this.huiColor;
        document.getElementById(`p${x}_${5}`).style.backgroundColor = this.blackColor;
        document.getElementById(`p${x}_${7}`).style.backgroundColor = this.blackColor;
        document.getElementById(`p${x}_${8}`).style.backgroundColor = this.huiColor;
        document.getElementById(`p${x}_${9}`).style.backgroundColor = this.redColor;
        document.getElementById(`p${x}_${10}`).style.backgroundColor = this.blackColor;
      }
      document.getElementById(`p${8}_${3}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${8}_${4}`).style.backgroundColor = this.huiColor;
      document.getElementById(`p${8}_${5}`).style.backgroundColor = this.huiColor;
      document.getElementById(`p${8}_${6}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${8}_${7}`).style.backgroundColor = this.huiColor;
      document.getElementById(`p${8}_${8}`).style.backgroundColor = this.huiColor;
      document.getElementById(`p${8}_${9}`).style.backgroundColor = this.blackColor;
      
      document.getElementById(`p${9}_${2}`).style.backgroundColor = this.blackColor;
      for(let i = 3; i <= 9; i++) {
        document.getElementById(`p${9}_${i}`).style.backgroundColor = this.huiColor;
      }
      document.getElementById(`p${9}_${10}`).style.backgroundColor = this.blackColor;

      for(let i = 10; i <= 11; i++) {
        document.getElementById(`p${i}_${1}`).style.backgroundColor = this.blackColor;
        for(let j = 2; j <= 10; j++) {
          document.getElementById(`p${i}_${j}`).style.backgroundColor = this.huiColor;
        }
        document.getElementById(`p${i}_${11}`).style.backgroundColor = this.blackColor;
      }

      document.getElementById(`p${12}_${0}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${12}_${1}`).style.backgroundColor = this.huiColor;
      document.getElementById(`p${12}_${2}`).style.backgroundColor = this.huiColor;
      document.getElementById(`p${12}_${3}`).style.backgroundColor = this.blackColor;
      for(let i = 4; i <= 8; i++) {
        document.getElementById(`p${12}_${i}`).style.backgroundColor = this.huiColor;
      }
      document.getElementById(`p${12}_${9}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${12}_${10}`).style.backgroundColor = this.huiColor;
      document.getElementById(`p${12}_${11}`).style.backgroundColor = this.huiColor;
      document.getElementById(`p${12}_${12}`).style.backgroundColor = this.blackColor;

      document.getElementById(`p${13}_${0}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${13}_${1}`).style.backgroundColor = this.huiColor;
      document.getElementById(`p${13}_${2}`).style.backgroundColor = this.huiColor;
      document.getElementById(`p${13}_${3}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${13}_${4}`).style.backgroundColor = this.rubaiColor;
      document.getElementById(`p${13}_${5}`).style.backgroundColor = this.rubaiColor;
      document.getElementById(`p${13}_${6}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${13}_${7}`).style.backgroundColor = this.rubaiColor;
      document.getElementById(`p${13}_${8}`).style.backgroundColor = this.rubaiColor;
      document.getElementById(`p${13}_${9}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${13}_${10}`).style.backgroundColor = this.huiColor;
      document.getElementById(`p${13}_${11}`).style.backgroundColor = this.huiColor;
      document.getElementById(`p${13}_${12}`).style.backgroundColor = this.blackColor;

      document.getElementById(`p${14}_${0}`).style.backgroundColor = this.blackColor;
      document.getElementById(`p${14}_${1}`).style.backgroundColor = this.huiColor;
      for(let i = 2; i <= 10; i++) {
        document.getElementById(`p${14}_${i}`).style.backgroundColor = this.rubaiColor;
      }
      document.getElementById(`p${14}_${11}`).style.backgroundColor = this.huiColor;
      document.getElementById(`p${14}_${12}`).style.backgroundColor = this.blackColor;

      document.getElementById(`p${15}_${1}`).style.backgroundColor = this.blackColor;
      for(let i = 2; i <= 10; i++) {
        document.getElementById(`p${15}_${i}`).style.backgroundColor = this.rubaiColor;
      }
      document.getElementById(`p${15}_${11}`).style.backgroundColor = this.blackColor;
      for(let i = 2; i <= 10; i++) {
        document.getElementById(`p${16}_${i}`).style.backgroundColor = this.blackColor;
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less">
.hello {
  width: 100vw;
  .page-wrap {
    width: 100vw;
    .item {
      background-color: #ffffff;
      float: left;
    }
  }
}
</style>
