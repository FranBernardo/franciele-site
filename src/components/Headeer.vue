<template>
  <header>
    <nav>
      <ul>
        <li>Sobre</li>
        <li>Contatos</li>
        <li>Tecnologia</li>
      </ul>
    </nav>
  </header>
</template>
<script>
export default {};
</script>
<style>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0px 15px;
  background: #716a5c;
  color: #ffffff;
}
header nav ul {
  display: flex;
  justify-content: space-around;
}
header nav li {
  display: flex;
  padding: 0px 5px;
  justify-content: space-around;
}
</style>