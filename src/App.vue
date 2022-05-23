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
// TASK 1 / OUTPUT WITH THE COMPOSITION API:
// export default {
//  const courseGoal = ref("Master Vue.js");
//  return { goal: courseGoal };
// }
// *****************************************************************

// TASK 2 / TOGGLE BUTTON VISIBILITY:
// import { ref } from "vue";
// 
// const courseGoal = ref("Master Vue.js");
// const isGoalVisible = ref(false);
// 
// function toggleGoal() {
//   goalIsVisible.value = !goalIsVisible.value
// }
// *****************************************************************

// TASK 3.1 / SEPARATE REFS:
// import { ref } from "vue";

// const courseGoal = ref("Master Vue.js");
// const isGoalVisible = ref(false);

// function toggleGoal() {
//   isGoalVisible.value = !isGoalVisible.value;
// }
// *****************************************************************

// TASK 3.2 / REF OBJECT:
// import { ref } from "vue";

// const courseData = ref({
//   goal: "Master Vue.js",
//   isVisible: false,
// });

// function toggleGoal() {
//   courseData.value.isVisible = !courseData.value.isVisible;
// }
// *****************************************************************

// TASK 3.3 / REACTIVE OBJECT:
// import { reactive } from "vue";

// const courseData = reactive({
//   goal: "Master Vue.js",
//   isVisible: false,
// });

// function toggleGoal() {
//   courseData.isVisible = !courseData.isVisible;
// }
</script> -->

<script>
// TASK 4 / OPTIONS API:
export default {
  data() {
    return {
      courseData: {
        goal: "Master Vue.js",
        isVisible: false,
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
