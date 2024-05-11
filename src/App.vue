<template>
  <header class="header">
    <button class="header__btn-back">
      <svg
        width="10"
        height="16"
        viewBox="0 0 10 16"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M9.03033 0.46967C9.2966 0.735936 9.3208 1.1526 9.10295 1.44621L9.03033 1.53033L2.561 8L9.03033 14.4697C9.2966 14.7359 9.3208 15.1526 9.10295 15.4462L9.03033 15.5303C8.76406 15.7966 8.3474 15.8208 8.05379 15.6029L7.96967 15.5303L0.96967 8.53033C0.703403 8.26406 0.679197 7.8474 0.897052 7.55379L0.96967 7.46967L7.96967 0.46967C8.26256 0.176777 8.73744 0.176777 9.03033 0.46967Z"
          fill="white"
        />
      </svg>
    </button>
    <div class="header__container-contact">
      <img src="@/assets/icon2.png" alt="icon" class="header__icon-img" />
      <span class="header__name-contact">Blond Treehorn Thug</span>
    </div>
    <button class="header__btn-menu">
      <svg
        width="18px"
        height="36px"
        viewBox="0 0 16 16"
        xmlns="http://www.w3.org/2000/svg"
        fill="#FFFFFF"
        class="bi bi-three-dots-vertical"
      >
        <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
        <g
          id="SVGRepo_tracerCarrier"
          stroke-linecap="round"
          stroke-linejoin="round"
        ></g>
        <g id="SVGRepo_iconCarrier">
          <path
            d="M9.5 13a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0zm0-5a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0zm0-5a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0z"
          ></path>
        </g>
      </svg>
    </button>
  </header>
  <main class="main" id="main">
    <div
      id="message"
      class="message"
      v-for="(message, index) in messages"
      :key="index"
      :class="messageleft(message.id) ? 'left' : 'right'"
    >
      <p
        class="message__text"
        :class="messageleft(message.id) ? 'text-left' : 'text-right'"
      >
        {{ message.text }}
      </p>
      <span
        class="message__time"
        :class="messageleft(message.id) ? 'time-left' : 'time-right'"
        >{{ message.time }}</span
      >
    </div>
  </main>
  <footer class="footer">
    <button class="footer__btn-add footer-btn">
      <svg
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M16.436 1C20.063 1 22.5 3.546 22.5 7.335V16.165C22.5 19.954 20.063 22.5 16.436 22.5H7.064C3.437 22.5 1 19.954 1 16.165V7.335C1 3.546 3.437 1 7.064 1H16.436ZM16.436 2.5H7.064C4.292 2.5 2.5 4.397 2.5 7.335V16.165C2.5 19.103 4.292 21 7.064 21H16.436C19.209 21 21 19.103 21 16.165V7.335C21 4.397 19.209 2.5 16.436 2.5ZM11.75 7.3273C12.164 7.3273 12.5 7.6633 12.5 8.0773V10.99L15.4165 10.9902C15.8305 10.9902 16.1665 11.3262 16.1665 11.7402C16.1665 12.1542 15.8305 12.4902 15.4165 12.4902L12.5 12.49V15.4043C12.5 15.8183 12.164 16.1543 11.75 16.1543C11.336 16.1543 11 15.8183 11 15.4043V12.49L8.0835 12.4902C7.6685 12.4902 7.3335 12.1542 7.3335 11.7402C7.3335 11.3262 7.6685 10.9902 8.0835 10.9902L11 10.99V8.0773C11 7.6633 11.336 7.3273 11.75 7.3273Z"
          fill="#F1C40F"
        />
      </svg>
    </button>
    <input
      type="text"
      class="footer__input-message"
      v-model="inputModel"
      @keyup.enter="inputMessage"
    />
    <div class="footer__container-btn-right">
      <button class="footer__btn-cash footer-btn">
        <svg
          height="24px"
          width="25px"
          version="1.1"
          id="Capa_1"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          viewBox="0 0 235.517 235.517"
          xml:space="preserve"
          fill="#000000"
        >
          <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
          <g
            id="SVGRepo_tracerCarrier"
            stroke-linecap="round"
            stroke-linejoin="round"
          ></g>
          <g id="SVGRepo_iconCarrier">
            <g>
              <path
                style="fill: #f1c40f"
                d="M118.1,235.517c7.898,0,14.31-6.032,14.31-13.483c0-7.441,0-13.473,0-13.473 c39.069-3.579,64.932-24.215,64.932-57.785v-0.549c0-34.119-22.012-49.8-65.758-59.977V58.334c6.298,1.539,12.82,3.72,19.194,6.549 c10.258,4.547,22.724,1.697,28.952-8.485c6.233-10.176,2.866-24.47-8.681-29.654c-11.498-5.156-24.117-8.708-38.095-10.236V8.251 c0-4.552-6.402-8.251-14.305-8.251c-7.903,0-14.31,3.514-14.31,7.832c0,4.335,0,7.843,0,7.843 c-42.104,3.03-65.764,25.591-65.764,58.057v0.555c0,34.114,22.561,49.256,66.862,59.427v33.021 c-10.628-1.713-21.033-5.243-31.623-10.65c-11.281-5.755-25.101-3.72-31.938,6.385c-6.842,10.1-4.079,24.449,7.294,30.029 c16.709,8.208,35.593,13.57,54.614,15.518v13.755C103.79,229.36,110.197,235.517,118.1,235.517z M131.301,138.12 c14.316,4.123,18.438,8.257,18.438,15.681v0.555c0,7.979-5.776,12.651-18.438,14.033V138.12z M86.999,70.153v-0.549 c0-7.152,5.232-12.657,18.71-13.755v29.719C90.856,81.439,86.999,77.305,86.999,70.153z"
              ></path>
            </g>
          </g>
        </svg>
      </button>
      <button class="footer__btn-camera footer-btn">
        <svg
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M15.3176 3.35442C15.9012 3.58673 16.3139 4.00545 16.6838 4.61932L16.8057 4.83118L17.258 5.69833L17.2728 5.72254L17.2864 5.74362L17.3248 5.79613C17.5308 6.02063 17.8756 6.15626 18.1032 6.15626C20.188 6.15626 21.8907 7.79352 21.9951 9.85179L22.0002 10.0523V15.8473C22.0002 18.5193 19.89 20.6997 17.2457 20.8127L17.0302 20.8173H6.9702C4.29754 20.8173 2.11767 18.7074 2.00479 16.0628L2.0002 15.8473V10.0523C2.0002 7.90085 3.74518 6.15626 5.8972 6.15626C6.12397 6.15626 6.46928 6.02043 6.67564 5.79613L6.68275 5.78775L6.69165 5.77609L6.74307 5.69721L7.19402 4.83146C7.59597 4.10093 8.03323 3.61258 8.68208 3.35433C9.87109 2.88155 14.1295 2.88155 15.3176 3.35442ZM9.23655 4.74809C9.01516 4.83621 8.81472 5.04017 8.60082 5.39376L8.50822 5.55456L8.12336 6.29866L8.02863 6.47009C7.94956 6.60161 7.87046 6.71264 7.78015 6.81105C7.31973 7.31151 6.65867 7.60056 6.07102 7.64898L5.8972 7.65626L5.7331 7.66179C4.54017 7.74245 3.58641 8.69598 3.50573 9.88825L3.5002 10.0523V15.8473C3.5002 17.6995 4.95194 19.2133 6.77981 19.3121L6.9702 19.3173H17.0302C18.8821 19.3173 20.3962 17.8649 20.4951 16.0376L20.5002 15.8473V10.0523C20.5002 8.78447 19.5144 7.74611 18.2673 7.66179L18.1032 7.65626L17.9291 7.64898C17.3405 7.60055 16.6795 7.31142 16.2196 6.81038C16.1305 6.71328 16.0519 6.60304 15.9732 6.47263L15.9544 6.4403L15.9318 6.40014L15.8158 6.1824L15.4918 5.55484C15.2731 5.15773 15.0728 4.91503 14.8566 4.79307L14.7628 4.74809L14.6435 4.70842C13.6144 4.41754 10.0346 4.43076 9.23655 4.74809ZM11.9999 9.19896C14.1701 9.19896 15.9289 10.9577 15.9289 13.128C15.9289 15.2982 14.1701 17.057 11.9999 17.057C9.82968 17.057 8.0709 15.2982 8.0709 13.128C8.0709 10.9577 9.82968 9.19896 11.9999 9.19896ZM11.9999 10.699C10.6581 10.699 9.5709 11.7862 9.5709 13.128C9.5709 14.4697 10.6581 15.557 11.9999 15.557C13.3417 15.557 14.4289 14.4697 14.4289 13.128C14.4289 11.7862 13.3417 10.699 11.9999 10.699ZM17.5045 8.49996C18.0568 8.49996 18.5045 8.94767 18.5045 9.49996C18.5045 10.0128 18.1185 10.4355 17.6211 10.4932L17.5045 10.5C16.9432 10.5 16.4955 10.0522 16.4955 9.49996C16.4955 8.98712 16.8815 8.56445 17.3789 8.50668L17.5045 8.49996Z"
            fill="#F1C40F"
          />
        </svg>
      </button>
      <button class="footer__btn-voice footer-btn">
        <svg
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M19.7495 9.8009C20.1645 9.8009 20.4995 10.1369 20.4995 10.5509C20.4995 15.1431 16.9749 18.9235 12.4998 19.3069L12.4995 21.75C12.4995 22.164 12.1635 22.5 11.7495 22.5C11.3355 22.5 10.9995 22.164 10.9995 21.75L11.0002 19.307C6.52465 18.924 2.99951 15.1434 2.99951 10.5509C2.99951 10.1369 3.33551 9.8009 3.74951 9.8009C4.16451 9.8009 4.49951 10.1369 4.49951 10.5509C4.49951 14.5689 7.75151 17.8389 11.7495 17.8389C15.7475 17.8389 18.9995 14.5689 18.9995 10.5509C18.9995 10.1369 19.3355 9.8009 19.7495 9.8009ZM11.7495 1C14.4025 1 16.5615 3.167 16.5615 5.831V10.519C16.5615 13.182 14.4025 15.349 11.7495 15.349C9.09651 15.349 6.93751 13.182 6.93751 10.519V5.831C6.93751 3.167 9.09651 1 11.7495 1ZM11.7495 2.5C9.92351 2.5 8.43751 3.994 8.43751 5.831V10.519C8.43751 12.354 9.92351 13.849 11.7495 13.849C13.5755 13.849 15.0615 12.354 15.0615 10.519V5.831C15.0615 3.994 13.5755 2.5 11.7495 2.5Z"
            fill="#F1C40F"
          />
        </svg>
      </button>
    </div>
  </footer>
</template>

<script>
import { ref, watch } from "vue";

export default {
  setup() {
    const messages = ref([
      { id: 1, text: `Where's the fucking money Lebowski?`, time: "12:02" },
      { id: 1, text: `Where's the fucking money, shithead?`, time: "12:04" },
      {
        id: 2,
        text: `It's uh... uh... it's down there somewhere, let me take another look`,
        time: "12:05",
      },
    ]);

    const messageleft = (id) => {
      if (id === 1) {
        return true;
      }
      return false;
    };
    const inputModel = ref("");

    const inputMessage = () => {
      const now = new Date();
      const hours = now.getHours().toString().padStart(2, "0");
      const minutes = now.getMinutes().toString().padStart(2, "0");
      const formattedTime = `${hours}:${minutes}`;
      const message = {
        id: 2,
        text: inputModel.value,
        time: formattedTime,
      };
      if (inputModel.value !== "") {
        messages.value.push(message);
        inputModel.value = "";
      }
    };

    return {
      messages,
      messageleft,
      inputMessage,
      inputModel,
    };
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  height: 100%;
  width: 100%;
  max-width: 768px;
  margin: 0 auto;
  background-color: #131313;
}

#app {
  position: relative;
  height: 100svh;
  overflow: hidden;
}

.header {
  position: absolute;
  z-index: 100;
  width: 100%;
  height: 59px;
  padding: 0 15px;
  background: #131313;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  top: 0;
}

.header__btn-back {
  background-color: transparent;
  border: none;
}

.header__container-contact {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 10px;
}

.header__icon-img {
  width: 36px;
  aspect-ratio: 1/1;
  border-radius: 100%;
  object-fit: cover;
  object-position: center;
}

.header__name-contact {
  font-family: "Roboto", sans-serif;
  font-weight: 700;
  font-size: 17px;
  line-height: 129%;
  letter-spacing: 0.03em;
  text-align: center;
  color: #fff;
}

.header__btn-menu {
  background-color: transparent;
  border: none;
}

.main {
  width: 100%;
  height: 100%;
  background-image: url("@/assets/fon.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  padding: 69px 10px;
  overflow: scroll;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}

.left {
  grid-column-start: 1; /* Начало в первой колонке */
  grid-column-end: 3; /* Конец во второй колонке */
}

.right {
  grid-column-start: 2; /* Начало в третьей колонке */
  grid-column-end: 4; /* Конец в четвертой колонке */
}

.message {
  background-color: transparent;
  display: flex;
  flex-direction: column;
}

.message__text {
  display: inline;
  border-radius: 25px 25px 25px 0;
  padding: 10px 10px 10px 20px;
  font-family: "Roboto", sans-serif;
  font-weight: 400;
  font-size: 15px;
  line-height: 147%;
  letter-spacing: 0.03em;
  color: #fff;
}

.text-right {
  border-radius: 25px 25px 0 25px;
  background-color: #1c6d78;
}

.text-left {
  border-radius: 25px 25px 25px 0;
  background-color: #131313;
}

.message__time {
  font-family: "Roboto", sans-serif;
  font-weight: 300;
  font-size: 10px;
  line-height: 220%;
  color: #eae6e6;
}

.time-right {
  text-align: end;
}

.footer {
  width: 100%;
  height: 59px;
  background: #131313;
  margin-top: auto;
  padding: 0 15px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  position: absolute;
  bottom: 0;
}

.footer__container-btn-right {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 10px;
}

.footer-btn {
  background-color: transparent;
  border: none;
}

.footer__input-message {
  min-width: 50%;
  height: 36px;
  background-color: #131313;
  border-radius: 20px;
  border: 1px solid white;
  padding: 0 10px;
  caret-color: white;
  color: white;
}

.footer__input-message:focus {
  outline: none;
}
</style>
