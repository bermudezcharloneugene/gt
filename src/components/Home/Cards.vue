<template>
    <div class="row mt-5" >
      <div v-scrollanimation class="col-sm-12 col-md-4" v-for="skill in skills" :key="skill.id">
          <div class="card p-3 text-center mb-5" v-show="showCards === true">
              <div class="card-head">
                <h4 class="card-title">{{skill.skillName}}</h4>
              </div>
              <hr>
              <div class="card-body">
                <p class="card-text">{{skill.skillSet}}</p>
              </div> 
          </div>
      </div>
    </div>
</template>

<script>

import data from '../../components/content.json'
export default {
  name: 'Cards',
  data() {
    return {
      skills: data.data,
      showCards: false
    }
  },
  methods: {
      showCard() {
          this.showCards = true
      }
  },
  created() {
      window.addEventListener("load", this.showCard);
  },
}
</script>

<style >
  .card {
    height: 300px;
  }

  .before-enter {
    opacity: 0;
    transform: translateX(300px);
    transition: all 1s ease-out;
  }

  .enter {
    opacity: 0;
    transform: translateX(0px);
    /* transition: opacity 1s; */
  }
</style>