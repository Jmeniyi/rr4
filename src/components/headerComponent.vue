<template>
  <div class="headerComponent">
    <div class="headerComponent__container">
      <div class="headerComponent__container_leftSide">
        <img src="../assets/img/logo.png">
        <button>ГЛАВНАЯ</button>
        <button>ВОДОЁМЫ</button>
        <button>ВИДЫ РЫБ</button>
        <div class="headerComponent__container_leftSide-dropDown">
          <button class="dropdown-toggle" type="button" id="dropdownMenuButton" data-toggle="dropdown"
            aria-haspopup="true" aria-expanded="false">
            ИНФО-БЛОК
          </button>
          <div class="dropdown">
            <button @click="isOpenDropdown = !isOpenDropdown" class="dropdown-toggle" type="button"
              id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
              ᐁ
            </button>
            <div v-if="isOpenDropdown" class="dropdown-menu" aria-labelledby="dropdownMenuButton">
              <a class="dropdown-item" href="#">Опция 1 Пользователя</a>
              <a class="dropdown-item" href="#">Опция 2</a>
              <a class="dropdown-item" href="#">Опция 3</a>
            </div>
          </div>
        </div>
      </div>
      <div class="headerComponent__container_rightSide">
        <span>Имя Пользователя</span>
        <button class="headerComponent__container_rightSide-userButton" @click="isOpenUser = !isOpenUser">
          <img src="../assets/img/user.svg">
          <span>ᐁ</span>
        </button>
        <div v-if="isOpenUser" class="dropdown-user" aria-labelledby="dropdownMenuButton">
          <a class="dropdown-item" href="#">Опция 1 Пользователя</a>
          <a class="dropdown-item" href="#">Опция 2</a>
          <a class="dropdown-item" href="#">Опция 3</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'headerComponent',
  data() {
    return {
      isOpenDropdown: false,
      isOpenUser: false
    }
  }
}
</script>

<style scoped>
.headerComponent {
  position: sticky;
  opacity: 1;
  height: 10%;
  width: 100%;
  background: #FFF;
  box-shadow: 0px 3px 8px 0px rgba(0, 0, 0, 0.10);
  -webkit-box-shadow: 0px 15px 15px -15px rgba(0, 138, 244, 0.267) inset;
  -moz-box-shadow: 0px -15px 15px -15px rgba(0, 138, 244, 0.34) inset;
  box-shadow: 0px -15px 15px -15px rgba(0, 138, 244, 0.286) inset;
}

.headerComponent__container {
  padding: 10px;
  display: flex;
}

.headerComponent__container_leftSide {
  width: fit-content;
  height: 100%;
  margin-inline: 5%;
  display: flex;
  justify-items: center;
  align-items: center;
}

.headerComponent__container_leftSide img {
  flex-shrink: 0;
  height: 60px;
  width: 60px;
  opacity: 0.8;
  margin-right: 50px;
}

.headerComponent__container_leftSide button {
  color: var(--Black, #2F2F2F);
  font-family: Montserrat;
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: 120%;
  background-color: inherit;
  border: none;
  margin-inline: 5%;
  white-space: nowrap;
}

.headerComponent__container_leftSide-dropDown {
  display: flex;
}

.dropdown-menu {
  position: absolute;
  width: fit-content;
  height: auto;
  padding: 10px;
  flex-direction: column;
  right: 40%;
  background-color: #ffffff;
  box-shadow: 0px 3px 8px 0px rgba(0, 0, 0, 0.10);
}

.dropdown-menu a {
  display: flex;
  height: auto;
  padding: 10px;
  text-decoration: none;
  color: var(--Black, #2F2F2F);
  font-family: Montserrat;
  font-size: 15px;
  font-style: normal;
  font-weight: 500;
  line-height: 120%;
}

.headerComponent__container_rightSide {
  position: relative;
  left: auto;
  right: 100px;
  margin-left: auto;
  width: auto;
  display: flex;
  align-items: center;
}

.headerComponent__container_rightSide-userButton {
  background-color: inherit;
  border: none;
  width: fit-content;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 5px;
  border: solid 1px;
  border-radius: 100px;
  margin-left: 20px;

}

.headerComponent__container_rightSide-userButton img {
  height: 40px;
  margin-right: 4px;
}

.headerComponent__container_rightSide-userButton h4 {
  font-weight: normal;
}

.dropdown-user {
  position: absolute;
  width: fit-content;
  height: auto;
  padding: 40px;
  flex-direction: column;
  right: -48%;
  top: 100%;
  background-color: #ffffff;
  box-shadow: 0px 3px 8px 0px rgba(0, 0, 0, 0.10);
}

.dropdown-user a {
  display: flex;
  height: auto;
  padding: 10px;
  text-decoration: none;
  color: var(--Black, #2F2F2F);
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  font-size: 15px;
  font-style: normal;
  font-weight: 500;
  line-height: 120%;
}</style>
