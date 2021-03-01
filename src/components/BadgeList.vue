<template>
  <section>
    <h2>Available Badges</h2>
    <ul>
      <li>
        <base-badge type="admin" caption="ADMIN"></base-badge>
      </li>
      <li>
        <base-badge type="author" caption="AUTHOR"></base-badge>
      </li>
      <li>
        <course-goal>
          <template #default="slotProps">
            <h2>{{ slotProps.item }}</h2>
            <p>{{ slotProps.anotherProp }}</p>
          </template>
        </course-goal>
      </li>
    </ul>
  </section>
</template>

<script>
import CourseGoal from './CourseGoal.vue';
export default {
  components: {
    CourseGoal
  }
}
</script>


<style>
section h2 {
  margin: 0.5rem 0;
  color: #3a3a3a;
}
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
}

li {
  margin-right: 1rem;
}
</style>