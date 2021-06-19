<template>
  <div class="body-center">
    <div class="container">
      <h3>Haftalık Planlarım</h3>
      <div class="row">
        <div class="col-md-3">
          <div class="top-panel">
            <h3>Pazartesi</h3>
            <button @click="pazartesiAdd" class="btn btn-secondary">
              <span>+</span>
            </button>
          </div>
          <input type="text" v-model="title" />
          <div v-for="pt in Pazartesi" :key="pt" class="task-panel">
            <input type="text" :value="pt" />
            <div @click="pazartesiDel(pt)" class="btn btn-danger">
              <i class="far fa-trash-alt"></i>
            </div>
          </div>
        </div>
        <div class="col-md-3">
          <div class="top-panel">
            <h3>Salı</h3>
            <button class="btn btn-secondary">
              <span>+</span>
            </button>
          </div>
          <div class="task-panel">
            <input type="text" />
            <div class="btn btn-danger">
              <i class="far fa-trash-alt"></i>
            </div>
          </div>
        </div>
        <div class="col-md-3">
          <div class="top-panel">
            <h3>Çarşamba</h3>
            <button class="btn btn-secondary">
              <span>+</span>
            </button>
          </div>
          <div class="task-panel">
            <input type="text" />
            <div class="btn btn-danger">
              <i class="far fa-trash-alt"></i>
            </div>
          </div>
        </div>
        <div class="col-md-3">
          <div class="top-panel">
            <h3>Perşembe</h3>
            <button class="btn btn-secondary">
              <span>+</span>
            </button>
          </div>
          <div class="task-panel">
            <input type="text" />
            <div class="btn btn-danger">
              <i class="far fa-trash-alt"></i>
            </div>
          </div>
        </div>
        <div class="col-md-3">
          <div class="top-panel">
            <h3>Cuma</h3>
            <button class="btn btn-secondary">
              <span>+</span>
            </button>
          </div>
          <div class="task-panel">
            <input type="text" />
            <div class="btn btn-danger">
              <i class="far fa-trash-alt"></i>
            </div>
          </div>
        </div>
        <div class="col-md-3">
          <div class="top-panel">
            <h3>Cumartesi</h3>
            <button class="btn btn-secondary">
              <span>+</span>
            </button>
          </div>
          <div class="task-panel">
            <input type="text" />
            <div class="btn btn-danger">
              <i class="far fa-trash-alt"></i>
            </div>
          </div>
        </div>
        <div class="col-md-3">
          <div class="top-panel">
            <h3>Pazar</h3>
            <button class="btn btn-secondary">
              <span>+</span>
            </button>
          </div>
          <div class="task-panel">
            <input type="text" />
            <div class="btn btn-danger">
              <i class="far fa-trash-alt"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "",
      Pazartesi: [],
      Salı: [],
      Çarşamaba: [],
      Perşembe: [],
      Cuma: [],
      Cumartes: [],
      Pazar: []
    };
  },
  methods: {
    pazartesiAdd() {
      this.Pazartesi.push(this.title);
      this.title = null;
      console.log(this.Pazartesi);
    },
    pazartesiDel(i) {
      this.Pazartesi.pop(i);
    }
  }
};
</script>
<style>
.body-center {
  width: 100%;
  height: 80vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
.col-md-3 {
  background-color: #dfeeea;
  height: 250px;
  width: calc(25% - 20px);
  padding-right: 10px;
  margin-right: 5px;
  padding: 13px;
  margin-bottom: 10px;
  border-radius: 5px;
}
.col-md-3:nth-of-type(3) {
  margin-right: 5;
}
.top-panel {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.top-panel h3 {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 16px;
  font-weight: bold;
}
.top-panel .btn-secondary {
  width: 30px;
  height: 30px;
  background-color: none;
  border-radius: 5px;
  align-items: center;
  justify-content: center;
  position: relative;
}
.top-panel .btn-secondary span {
  position: absolute;
  left: 25%;
  bottom: -10%;
  font-size: 23px;
  font-weight: 800;
}
.task-panel {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 5px;
}
.task-panel input[type="text"] {
  border: none;
  outline: none;
  height: 30px;
  width: 200px;
}
.task-panel .btn-danger {
  display: block;
  height: 30px;
  text-align: center;
  align-content: center;
  justify-content: center;
  position: relative;
}
.task-panel .btn-danger i {
  position: absolute;
  left: 25%;
  top: 25%;
}
</style>