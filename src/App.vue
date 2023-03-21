<template>
  <template></template>
  <div
    class="bg-dark vh-100 px-5 d-flex align-items-center justify-content-center">
    <div
      class="container-xxl rounded-3 h-50 bg-dark border border-2 p-5 text-white">
      <div class="row mb-4">
        <div class="col d-flex">
          <label class="mb-1" for="table-name__input">
            Название таблицы:
          </label>
          <input
            class="ms-2 rounded-3 border-0 bg-gray"
            type="text"
            id="table-name__input"
            autocomplete="off" />
        </div>
      </div>

      <div class="row border-primary border d-flex bg-secondary">
        <div class="filter__inner"></div>
        <button class="rounded-circle bg-success w-1">+</button>
        <input
          class="filter__count"
          type="number"
          id="filter__count"
          placeholder="10x"
          value="5" />
      </div>

      <button class="button-create-code">Скомпилировать код</button>

      <div class="row">
        <div class="result__title">Ваш код:</div>
        <button class="result__copy">Скопировать всё</button>
        <output class="result__output"> </output>
      </div>
    </div>

    <div class="filter-popup" style="display: none">
      <div class="filter-popup__inner">
        <div class="filter-popup__cross">
          <svg
            version="1.1"
            id="Capa_1"
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            x="0px"
            y="0px"
            viewBox="0 0 490 490"
            style="enable-background: new 0 0 490 490"
            xml:space="preserve">
            <polygon
              fill="#f8f8f2"
              points="11.387,490 245,255.832 478.613,490 489.439,479.174 255.809,244.996 489.439,10.811 478.613,0 245,234.161
             11.387,0 0.561,10.811 234.191,244.996 0.561,479.174 " />
          </svg>
        </div>
        <div class="filter-popup__name-field">
          <label
            class="filter-popup__name-field-label"
            for="filter-popup__name-field-input">
            Название столбца:
          </label>
          <input
            type="text"
            class="filter-popup__name-field-input"
            id="filter-popup__name-field-input" />
        </div>

        <div class="filter-popup__select-wrapper">
          <select class="filter-popup__select" id="filter-popup__select">
            <option value="surname">Фамилия</option>
            <option value="name">Имя</option>
            <option value="age">Возраст</option>
          </select>
        </div>

        <div class="filter-popup__uniq uniq">
          <!-- <div class="uniq__range uniq__item"></div> -->
          <div class="uniq__checkbox uniq__item">
            <div class="uniq__checkbox-wrapper">
              <input
                class="uniq__checkbox-input"
                id="uniq__checkbox-input-pk"
                type="checkbox" />
              <label class="uniq__checkbox-label" for="uniq__checkbox-input-pk">
                PRIMARY KEY:
              </label>
            </div>
            <div class="uniq__checkbox-wrapper">
              <input
                class="uniq__checkbox-input"
                id="uniq__checkbox-input-fk"
                type="checkbox" />
              <label class="uniq__checkbox-label" for="uniq__checkbox-input-fk">
                FOREIGN KEY:
              </label>
            </div>
          </div>
        </div>

        <!-- <label class="add-filter-fk" for="filter-popup__fk-checkbox">
              FK:
            </label>

            <input
              class="filter-popup__fk-checkbox"
              type="checkbox"
              id="filter-popup__fk-checkbox"
            /> -->

        <button class="filter-popup__btn-add">Добавить</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>
