<template>
  <div class="issue-form flex-column flex-align-start">
    <div class="form-row">
      <label>Координаты</label>
      <div class="field">
        <!--  todo: Вывести координаты проблемы  -->
        <span>широта: </span>
        <span>долгота: </span>
      </div>
    </div>
    <div class="form-row">
      <label>Название</label>
      <div class="field">
        <input type="text"/>
      </div>
    </div>
    <div class="form-row">
      <label>Описание</label>
      <div class="field">
        <textarea />
      </div>
    </div>
    <div class="form-row">
      <label>Цена</label>
      <div class="field">
        <input type="text">
      </div>
    </div>
    <div class="form-row">
      <label>Программа</label>
      <div class="field">
        <select>
          <option value="1">Программа 1</option>
          <option value="2">Программа 2</option>
          <option value="3">Программа 3</option>
          <option value="4">Программа 4</option>
          <option value="5">Программа 5</option>
        </select>
      </div>
    </div>
    <div class="submit-row">
      <div class="button" @click="onClickSubmit">
        Сохранить
      </div>
    </div>
  </div>
</template>

<script>
// todo: Реализовать отображение/редактирование данных из объекта
export default {
  name: 'IssueForm',
  props: {
    issue: Object
  },
  methods: {
    onClickSubmit() {
      // todo: Реализовать сохранение изменений
    }
  }
}
</script>

<style scoped lang="scss">
  .issue-form {
    gap: 10px;

    .form-row {
      display: flex;
      flex-direction: column;
      label {
        text-align: left;
      }
    }

    .submit-row {
      .button {
        padding: 10px;
        font-weight: bold;
        background-color: limegreen;
      }
    }
  }
</style>
