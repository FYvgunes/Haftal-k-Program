<template>
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
        <input class="form-control mt-2" type="text" v-model="Monday" />
        <div v-for="pt in Pazartesi" :key="pt" class="task-panel">
          <h6>{{ pt }}</h6>
          <div @click="pazartesiDel(pt)" class="btn btn-danger">
            <i class="far fa-trash-alt"></i>
          </div>
        </div>
      </div>
      <div class="col-md-3">
        <div class="top-panel">
          <h3>Salı</h3>
          <button @click="saliAdd" class="btn btn-secondary">
            <span>+</span>
          </button>
        </div>
        <input class="form-control mt-2" type="text" v-model="Tueday" />

        <div v-for="say in Salı" :key="say" class="task-panel">
          <h6>{{ say }}</h6>
          <div @click="SaliDel(say)" class="btn btn-danger">
            <i class="far fa-trash-alt"></i>
          </div>
        </div>
      </div>
      <div class="col-md-3">
        <div class="top-panel">
          <h3>Çarşamba</h3>
          <button @click="carsambaAdd" class="btn btn-secondary">
            <span>+</span>
          </button>
        </div>
        <input class="form-control mt-2" type="text" v-model="Weknesday" />

        <div v-for="car in Carsamba" :key="car" class="task-panel">
          <h6>{{ car }}</h6>
          <div @click="cardel(car)" class="btn btn-danger">
            <i class="far fa-trash-alt"></i>
          </div>
        </div>
      </div>
      <div class="col-md-3">
        <div class="top-panel">
          <h3>Perşembe</h3>
          <button @click="persembeAdd" class="btn btn-secondary">
            <span>+</span>
          </button>
        </div>
        <input class="form-control mt-2" type="text" v-model="Thursday" />

        <div v-for="per in Persembe" :key="per" class="task-panel">
          <h6>{{ per }}</h6>
          <div @click="perdel(per)" class="btn btn-danger">
            <i class="far fa-trash-alt"></i>
          </div>
        </div>
      </div>
      <div class="col-md-3">
        <div class="top-panel">
          <h3>Cuma</h3>
          <button @click="cumadd" class="btn btn-secondary">
            <span>+</span>
          </button>
        </div>
        <input class="form-control mt-2" type="text" v-model="Friday" />

        <div v-for="friday in Cuma" :key="friday" class="task-panel">
          <h6>{{ friday }}</h6>
          <div @click="cumdel(friday)" class="btn btn-danger">
            <i class="far fa-trash-alt"></i>
          </div>
        </div>
      </div>
      <div class="col-md-3">
        <div class="top-panel">
          <h3>Cumartesi</h3>
          <button @click="saturdayadd" class="btn btn-secondary">
            <span>+</span>
          </button>
        </div>
        <input class="form-control mt-2" type="text" v-model="Saturday" />

        <div v-for="saturday in Cumartes" :key="saturday" class="task-panel">
          <h6>{{ saturday }}</h6>
          <div @click="saturdayDel(saturday)" class="btn btn-danger">
            <i class="far fa-trash-alt"></i>
          </div>
        </div>
      </div>
      <div class="col-md-3">
        <div class="top-panel">
          <h3>Pazar</h3>
          <button @click="sundayAdd" class="btn btn-secondary">
            <span>+</span>
          </button>
        </div>
        <input class="form-control mt-2" type="text" v-model="sunday" />

        <div v-for="sunday in Pazar" :key="sunday" class="task-panel">
          <h6>{{ sunday }}</h6>
          <div @click="sundayDel(sunday)" class="btn btn-danger">
            <i class="far fa-trash-alt"></i>
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
      Monday: "",
      Tueday: "",
      Weknesday: "",
      Thursday: "",
      Friday: "",
      Saturday: "",
      sunday: "",
      Pazartesi: [],
      Salı: [],
      Carsamba: [],
      Persembe: [],
      Cuma: [],
      Cumartes: [],
      Pazar: []
    };
  },
  methods: {
    pazartesiAdd() {
      this.Pazartesi.push(this.Monday);
      this.Monday = null;
    },
    pazartesiDel(i) {
      this.Pazartesi.pop(i);
    },
    saliAdd() {
      this.Salı.push(this.Tueday);
      this.Tueday = null;
    },
    SaliDel(i) {
      this.Salı.pop(i);
    },
    carsambaAdd() {
      this.Carsamba.push(this.Weknesday);
      this.Weknesday = null;
    },
    cardel(i) {
      this.Carsamba.pop(i);
    },
    persembeAdd() {
      this.Persembe.push(this.Thursday);
      this.Thursday = null;
    },
    perdel(i) {
      this.Persembe.pop(i);
    },
    cumadd() {
      this.Cuma.push(this.Friday);
      this.Friday = null;
    },
    cumdel(i) {
      this.Cuma.pop(i);
    },
    saturdayadd() {
      this.Cumartes.push(this.Saturday);
      this.Saturday = "";
    },
    saturdayDel(i) {
      this.Cumartes.pop(i);
    },
    sundayAdd() {
      this.Pazar.push(this.sunday);
      this.sunday = "";
    },
    sundayDel(i) {
      this.Pazar.pop(i);
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
  height: 300px;
  width: calc(25% - 15px);
  padding-right: 10px;
  margin-right: 5px;
  padding: 13px;
  margin-bottom: 10px;
  border-radius: 5px;
}
.col-md-3:nth-of-type(3) {
  margin-right: 5;
}
@media (max-width: 960px) {
  .col-md-3 {
    width: calc(50% - 15px);
  }
}

@media (max-width: 360px) {
  .col-md-3 {
    width: calc(100% - 0px);
  }
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