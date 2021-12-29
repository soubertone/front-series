<template>
  <div class="container-fluid px-2">
    <Header></Header>
    <ul class="list-group px-2">
      <li class="list-group-item" v-for="serie in series" :key="serie.id">
        <div class="row">

          <div class="col-10">
            <a class="font-weight-light text-decoration-none" href="#">{{ serie.name }}</a>
          </div>
          <div class="col-2 d-flex justify-content-end">
            <button class="btn btn-primary btn-sm mx-2">
              <i class="bi bi-pencil-square"></i>
            </button>
            <button class="btn btn-outline-danger btn-sm">
              <i class="bi bi-trash"></i>
            </button>
          </div>

        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import Header from '@/components/Layout/Header.vue';

export default {

  data() {
    return {
      series: [
        {
          id: 1,
          name: "Lost", 
        },
        {
          id: 2,
          name: "Arrow", 
        },
        {
          id: 3,
          name: "The Flash", 
        },
        {
          id: 4,
          name: "Suits", 
        },
      ]
    }
  },

  components: {
    Header
  }
}
</script>