<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
    <div class="card" style="margin-bottom:10px">
      <div class="panel-body quote">
        <slot></slot>
      </div>
    </div>
  </div>
</template>
<script></script>
<style>
.panel-body {
  font-family: "Arizonia", cursive;
  font-size: 24px;
  color: #6e6e6e;
  border: 1px solid black;
}
.quote {
  cursor: pointer;
}
.quote:hover {
  background-color: #ffe2e2;
}
</style>
