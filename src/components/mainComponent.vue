<template>
    <div class="mainComponent">
        <div class="mainComponent__galery">
            <div class="mainComponent__galery_card" v-for="i in 30" :key="i">
                <img src="../assets/img/lesh.jpg">
                <div class="mainComponent__galery_card-details">
                    <h3>Лещ</h3>
                    <p>Старый острог</p>
                    <a href="#" class="button">Подробнее</a>
                    <h2>Имя пользователя</h2>
                    <img src="../assets/img/heart.svg" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<style>
.mainComponent {
    height: 100vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.mainComponent__galery {
    height: 100vh;
    width: 90%;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    justify-content: space-between;
}

.mainComponent__galery_card {
    position: relative;
    height: 55%;
    width: 32%;
    margin: 20px 0px 10px 5px;
    display: flex;
    flex-direction: column;
    border-radius: 10px;
    box-shadow: 0px 3px 8px 0px rgba(0, 0, 0, 0.10);
}

.mainComponent__galery_card img {
    width: 100%;
    height: auto;
    margin-bottom: 10px;
    object-fit: contain;
    flex-shrink: 0;
}

.mainComponent__galery_card-details {
    display: flex;
    flex-direction: column;
    margin: 20px 0px 10px 15px;
    letter-spacing: 1px;

}

.mainComponent__galery_card-details img {
    height: 20px;
    width: 20px;
    padding: 0px 10px 20px 0px;
    position: absolute;
    top: 10px;
    right: 0;
}
.mainComponent__galery_card-details h3 {
    color: var(--Black, #2F2F2F);
    font-family: Montserrat;
    font-size: 20px;
    font-style: normal;
    font-weight: 500;
    line-height: 120%;
}

.mainComponent__galery_card-details p {
    color: var(--Black, #2F2F2F);
    font-family: Montserrat;
    font-size: 20px;
    font-style: normal;
    font-weight: 500;
    line-height: 120%;
    margin: 7px 0px 7px 0px;
}

.mainComponent__galery_card-details span {
    color: var(--Black, #2F2F2F);
    font-family: Montserrat;
    font-size: 20px;
    font-style: normal;
    font-weight: 500;
    line-height: 120%;

}

.mainComponent__galery_card-details h2 {
    color: var(--Black, #2F2F2F);
    font-family: Montserrat;
    font-size: 20px;
    font-style: normal;
    font-weight: 500;
    line-height: 120%;
    text-align: left;
}
</style>