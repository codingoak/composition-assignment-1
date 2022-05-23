<template>
  <h2>My Course Goal</h2>
  <!-- Task 1: Output your main course goal with help of the composition API -->
  <!-- Don't hardcode it into the template, instead hardcode it into the JS code -->
  <h3 v-if="courseData.isVisible">{{ courseData.goal }}</h3>
  <!-- Task 2: Toggle (show/ hide) the goal with help of the button  -->
  <button @click="toggleGoal">Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<!-- <script setup>
// SEPARATE REFS:
// import { ref } from "vue";

// const courseGoal = ref("Master Vue.js");
// const isGoalVisible = ref(true);

// function toggleGoal() {
//   isGoalVisible.value = !isGoalVisible.value;
// }
// *****************************************************************

// REF OBJECT:
// import { ref } from "vue";

// const courseData = ref({
//   goal: "Master Vue.js",
//   isVisible: true,
// });

// function toggleGoal() {
//   courseData.value.isVisible = !courseData.value.isVisible;
// }
// *****************************************************************

// REACTIVE OBJECT:
// import { reactive } from "vue";

// const courseData = reactive({
//   goal: "Master Vue.js",
//   isVisible: true,
// });

// function toggleGoal() {
//   courseData.isVisible = !courseData.isVisible;
// }
</script> -->

<script>
export default {
  data() {
    return {
      courseData: {
        goal: "Master Vue.js",
        isVisible: true,
      },
    };
  },
  methods: {
    toggleGoal() {
      this.courseData.isVisible = !this.courseData.isVisible;
    },
  },
};
</script>

<style>
html {
  font-family: sans-serif;
}
body {
  margin: 3rem;
  text-align: center;
}
</style>
