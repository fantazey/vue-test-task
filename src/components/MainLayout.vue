<template>
  <div class="flex-row flex-justify-between">
    <div style="flex-grow:2" class="flex-column left-side">
      <h3>Списки</h3>
      <div class="flex-row flex-justify-evenly list-type-selector">
        <a :class="{ 'button': true,'active': isIssuesActive }" @click="toggleIssues">Проблемы</a>
        <a :class="{ 'button': true,'active': isTaksActive }" @click="toggleTasks">Задачи</a>
      </div>
      <items-list :items="items"></items-list>
    </div>
    <div style="flex-grow:2" class="flex-column right-side">
      <h3>Формы</h3>
      <div class="card-wrapper">
        <issue-form :issue="{}"/>
      </div>
    </div>
  </div>
</template>

<script>
import ItemsList from '@/components/ItemsList'
import IssueForm from '@/components/IssueForm'
const ISSUES_TAB = 'ISSUES';
const TASK_TAB = 'TASKS';
export default {
  name: 'MainLayout',
  components: { IssueForm, ItemsList },
  data() {
    return {
      activeTab: ISSUES_TAB,
      items: [
        {
          id: 1,
          name: 'Test-1',
          solution: 'foo bar',
          longitude: 34.232,
          latitude: 59.1231,
          price: 900000,
          program: 1,
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio, saepe.'
        },
        {
          id: 2,
          name: 'Test-2',
          solution: 'foo bar',
          longitude: 34.232,
          latitude: 59.1231,
          price: 600000,
          program: 1,
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio, saepe.'
        },
        {
          id: 3,
          name: 'Test-3',
          solution: 'foo bar',
          longitude: 34.232,
          latitude: 59.1231,
          price: 100000,
          program: 4,
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio, saepe.'
        }
      ],
      isIssuesActive: true,
      isTasksActive: false
    }
  },
  methods: {
    toggleIssues() {
      this.activeTab = ISSUES_TAB;
    },
    toggleTasks() {
      this.activeTab = TASK_TAB;
    }
  }
}
</script>

<style scoped lang="scss">
  .left-side {
    padding: 0 10px;
    border-right: 1px solid black;
    .list-type-selector {
      .active {
        font-weight: bolder;
      }
    }
  }
  .right-side {
    padding: 0 10px;
  }
</style>
