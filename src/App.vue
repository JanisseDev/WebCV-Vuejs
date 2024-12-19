<script setup>
import { ref, onMounted, provide, watch } from 'vue'
import Cv from './Cv.vue'

const showLink = ref(true);
provide('showLink', showLink);

const thickerText = ref(false);
provide('thickerText', thickerText);

const colorless = ref(false);
provide('colorless', colorless);

const showMonth = ref(false);
provide('showMonth', showMonth);

const phone = ref('');
provide('phone', phone);
watch(phone, (value) => {
  localStorage.phone = value;
});

const mail = ref('');
provide('mail', mail);
watch(mail, (value) => {
  localStorage.mail = value;
});

onMounted(() => {
  if(localStorage.phone) {
    phone.value = localStorage.phone;
  }
  if(localStorage.mail) {
    mail.value = localStorage.mail;
  }
})

const delay = ms => new Promise(res => setTimeout(res, ms));

function printCv() {
    let mywindow = window.open(' ', 'PRINT', 'height=1188,width=840,top=0,left=0');

    mywindow.document.write('<html>');
    mywindow.document.write(document.head.innerHTML);
    mywindow.document.write('<body style="margin:0; padding:0; background-color:white";>');
    mywindow.document.write(document.getElementsByClassName("printable")[0].outerHTML);
    mywindow.document.write('</body></html>');

    mywindow.document.close(); // necessary for IE >= 10
    mywindow.focus(); // necessary for IE >= 10*/

    mywindow.onload = async function () {
        await delay(200);
        mywindow.print();
        mywindow.close();
    }

    return true;
}

function toggleLinks() {
  showLink.value = !showLink.value;
}

function toggleThickerText() {
  thickerText.value = !thickerText.value;
}

function toggleColorless() {
  colorless.value = !colorless.value;
}

function toggleMonths() {
  showMonth.value = !showMonth.value;
}

function optimizePrint() {
  showLink.value = false;
  thickerText.value = true;
}
</script>

<template>
  <main>
    <Cv class="printable"/>
    <div class="options">
      <button @click="printCv">Print</button>
      <button @click="toggleLinks">Toggle links</button>
      <button @click="toggleThickerText">Toggle thicker texts</button>
      <button @click="toggleColorless">Toggle colorless mode</button>
      <button @click="toggleMonths">Toggle Months</button>
      <br>
      <button @click="optimizePrint">Optimize print</button>
      <br>
      <input v-model="phone" placeholder="phone number" />
      <input v-model="mail" placeholder="mail address" />
    </div>
  </main>
</template>

<style scoped>
main {
  display: flex;
  gap: 10px;
}

.options {
  display: flex;
  flex-direction: column;
}
</style>