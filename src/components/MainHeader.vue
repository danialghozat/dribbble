<template>
  <main class="container">
    <section class="postType">
      <div class="postName">Popular</div>
      <div class="downArrow"></div>
    </section>
    <section class="cardType">
      <ul>
        <li class="category" @click="activeClass">All</li>
        <li class="category">Animation</li>
        <li class="category">Branding</li>
        <li class="category">lllustration</li>
        <li class="category">Mobile</li>
        <li class="category">Print</li>
        <li class="category">Product Design</li>
        <li class="category">Typography</li>
        <li class="category">Web Design</li>
      </ul>
    </section>
    <section class="filter">
      <div class="filterLogo">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" role="img" class="icon filter-icon icon-14">
          <path fill-rule="evenodd" clip-rule="evenodd" d="M0 6C0 5.17157 0.671573 4.5 1.5 4.5H22.5C23.3284 4.5 24 5.17157 24 6C24 6.82843 23.3284 7.5 22.5 7.5H1.5C0.671573 7.5 0 6.82843 0 6ZM3 12C3 11.1716 3.67157 10.5 4.5 10.5H19.5C20.3284 10.5 21 11.1716 21 12C21 12.8284 20.3284 13.5 19.5 13.5H4.5C3.67157 13.5 3 12.8284 3 12ZM7.5 16.5C6.67157 16.5 6 17.1716 6 18C6 18.8284 6.67157 19.5 7.5 19.5H16.5C17.3284 19.5 18 18.8284 18 18C18 17.1716 17.3284 16.5 16.5 16.5H7.5Z"></path>
        </svg>
      </div>
      <span class="filter">Filters</span>
    </section>
  </main>
</template>

<script>
export default {
  name: "MainHeader",
}
</script>

<style>
main.container {
  width: 100%;
  height: 40px;
  display: flex;
  justify-content: space-between;
  /*border: 1px solid #eee;*/
}

section.postType {
  width: 8%;
  height: 100%;
  border: 2px solid #eee;
  border-radius: 10px;
  position: relative;
  transition: border 350ms,box-shadow 350ms;
}

section.postType:hover {
  cursor: pointer;
  border-radius: 10px;
  box-shadow: 0 0 0 3px #ff75a8;
  border: 1px solid #ff75a8;
}


section.postType div.postName {
  height: 98%;
  padding: 8px 35px 6px 16px;
  transition: color 0.5s;
}

section.postType:hover div.postName {
  color: #000;
}

section.postType div.downArrow {
  position: absolute;
  top: 14px;
  right: 15px;
  width: 7px;
  height: 7px;
  border-top: 2px solid #999999;
  border-right: 2px solid #999999;
  transform: rotate(135deg);
}

section.cardType {
  height: 100%;
  display: flex;
}

ul {
  list-style: none;
  display: flex;
  align-items: center;
  transition: color 0.5s;
}

li.category {
  margin: 0 5px;
  padding: 10px 12px;
  color: #6e6d7a;
  border-radius: 10px;
}
li.category:first-child {
  background-color: #eee;
  color: #000;
  font-weight: bold;
}

li:hover {
  color: #000;
  cursor: pointer;
}

section.filter {
  width: 7%;
  height: 100%;
  border: 2px solid #eee;
  border-radius: 10px;
  position: relative;
}

section.filter:hover {
  border: 2px solid #9e9ea7;
  cursor: pointer;
}


div.filterLogo {
  position: absolute;
  width: 20px;
  height: 20px;
  top: 8px;
  left: 12px;
}

div.filterLogo svg {
  fill: #000;
  width: 12px;
  height: 12px;
}


span.filter {
  position: absolute;
  top: 7px;
  right: 18px;
  font-size: 18px;
  color: #000;
  padding: 0 0 0 30px;
  font-weight: 100;
}







/*.active {*/
/*  background-color: #9e9ea7;*/
/*  border-radius: 10px;*/
/*  font-weight: bold;*/
/*}*/
</style>