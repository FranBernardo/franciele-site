<template>
  <div class="toggle-container">
    <label class="toggle">
      <input
        type="checkbox"
        :checked="mode === 'dark' ? 'checked' : false"
        @change="$emit('toggle')"
      />
      <span class="toggler round"></span>
    </label>
  </div>
</template>
<script>
export default {
  props: ["mode"],
};
</script>
<style>
.toggle {
  position: relative;
  display: inline-block;
  width: 60px;
  height: 34px;
}

.toggle input {
  opacity: 0;
  width: 0;
  height: 0;
}
.toggler {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: #07020d;
  -webkit-transition: 0.4s;
  transition: 0.4s;
}

.toggler::before {
  position: absolute;
  content: "";
  height: 26px;
  width: 26px;
  left: 4px;
  bottom: 4px;
  background: #716a5c;
  -webkit-transition: 0.4s;
  transition: 0.4s;
}

input:checked + .toggler {
  background: #f1e9db;
}
input:focus + .toggler {
  box-shadow: #07020d;
}
input:checked + .toggler::before {
  -webkit-transform: translateX(26px);
  -ms-transform: translateX(26px);
  transform: translateX(26px);
}

.toggler.round {
  border-radius: 34px;
}

.toggler.round::before {
  border-radius: 50%;
}
</style>