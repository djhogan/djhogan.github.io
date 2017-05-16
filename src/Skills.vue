<template>
  <div id="skills">
    <div v-for="skill in skills">
      {{ skill.category }}
      <div v-for="tech in skill.techs">
        {{ tech }} 
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'skills',
  data: {
    skills: [
      {
        category: "Big-Data",
        techs: [
          "Weka",
          "TensorFlow",
        ],
      },
      {
        category: "Mobile",
        techs: [
          "Android Studio",
        ],
      },
      {
        category: "Systems",
        techs: [
          "C",
          "C++",
          "Java",
        ],
      },
      { 
        category: "Scripting",
        techs: [
          "Python",
          "Ruby",
          "Perl",
        ],
      },
    ],
  },
}
</script>
