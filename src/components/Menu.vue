<template>
<div  :class="['mdc-select', 'mdc-select--outlined', 'select', idS]" style="width: 100%" >
  <div class="mdc-select__anchor" aria-labelledby="outlined-select-label">
    <span class="mdc-notched-outline">
      <span class="mdc-notched-outline__leading"></span>
      <span class="mdc-notched-outline__notch">
        <span id="outlined-select-label" class="mdc-floating-label">{{ title }}</span>
      </span>
      <span class="mdc-notched-outline__trailing"></span>
    </span>
    <span class="mdc-select__selected-text-container">
      <span id="demo-selected-text" class="mdc-select__selected-text"></span>
    </span>
    <span class="mdc-select__dropdown-icon">
      <svg
          class="mdc-select__dropdown-icon-graphic"
          viewBox="7 10 10 5" focusable="false">
        <polygon
            class="mdc-select__dropdown-icon-inactive"
            stroke="none"
            fill-rule="evenodd"
            points="7 10 12 15 17 10">
        </polygon>
        <polygon
            class="mdc-select__dropdown-icon-active"
            stroke="none"
            fill-rule="evenodd"
            points="7 15 12 10 17 15">
        </polygon>
      </svg>
    </span>
  </div>

  <!-- Other elements from the select remain. -->
  <div class="mdc-select__menu mdc-menu mdc-menu-surface mdc-menu-surface--fullwidth menu-type">
    <ul class="mdc-deprecated-list">
      <li class="mdc-deprecated-list-item mdc-deprecated-list-item--selected" data-value="1" aria-selected="true">
        <span class="mdc-deprecated-list-item__ripple"></span>
        <span class="mdc-deprecated-list-item__text">Пост</span>
      </li>
      <li class="mdc-deprecated-list-item" data-value="2">
        <span class="mdc-deprecated-list-item__ripple"></span>
        <span class="mdc-deprecated-list-item__text">Пост (Одноцветный)</span>
      </li>
    </ul>
  </div>
</div>

</template>

<script>
export default{
  props: ['title', 'idS'],
  
}
</script>
<style lang="scss">
@use "@material/list/mdc-list";
@use "@material/menu-surface/mdc-menu-surface";
@use "@material/menu/mdc-menu";
@use "@material/select/styles";
</style>