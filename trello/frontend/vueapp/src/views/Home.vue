<template>
  <div id="home">
    <!--头部-->
    <header>
      <div class="left">
        <a href class="btn btn-icon">
          <i class="icon icon-home"></i>
        </a>
        <a href class="btn btn-icon">
          <i class="icon icon-board"></i>
          <span class="txt">看板</span>
        </a>
      </div>
      <a href="/" class="logo"></a>
      <div class="right">
        <a href class="btn btn-icon">
          <i class="icon icon-add"></i>
        </a>
        <button class="avatar">
          <span>Z</span>
        </button>
      </div>
    </header>

    <main>
      <h2>
        <span class="icon icon-board"></span>
        我的看板
      </h2>
      <ul class="board-items">
        <li class="board-item">
          <span class="title">test</span>
        </li>
        <li class="board-item">
          <span class="title">共同努力吧！</span>
        </li>
        <li class="board-item">
          <span class="title">Welcome Board</span>
        </li>
        <li class="board-item create-new-board">
          <textarea class="title form-field-input" placeholder="创建新看板"></textarea>
        </li>
      </ul>
    </main>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>