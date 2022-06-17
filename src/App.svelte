<script lang="ts">
  import { fly } from "svelte/transition"
  let isOpen = false

  function handleClick() {
    isOpen = !isOpen
  }
</script>

<svelte:head>
  <title>หมอหมึก</title>
  <meta
    name="description"
    content="ผู้มีประสบการณ์พยากรณ์มากกว่า 10 ปี พร้อมคำพยากรณ์ที่แม่นยำ"
  />

  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link
    rel="preconnect"
    href="https://fonts.gstatic.com"
    crossorigin="anonymous"
  />
  <link
    href="https://fonts.googleapis.com/css2?family=Pridi:wght@200;300;400&display=swap"
    rel="stylesheet"
  />
</svelte:head>

<body class="bg-[#612378] text-white relative">
  {#if isOpen}
    <div
      transition:fly={{ y: 100, duration: 500 }}
      class="fixed p-6 top-0 bg-purple-400 w-screen h-screen z-50 flex flex-col items-center"
    >
      <button on:click={handleClick} class="relative w-full mb-6">
        <div class="relative h-6 w-6 mx-auto">
          <div class="absolute inset-x-0 top-1/2 h-[2px] rotate-45 bg-white" />
          <div class="absolute inset-x-0 top-1/2 h-[2px] -rotate-45 bg-white" />
        </div>
      </button>

      <ul class="flex flex-col items-center gap-2">
        <li class="">
          <a href="http://12.jwc.in.th" class="hover:underline"
            >เกี่ยวกับหมอหมึก</a
          >
        </li>
        <li class="">
          <a href="http://12.jwc.in.th" class="hover:underline">บทความ</a>
        </li>
        <li class="">
          <a href="http://12.jwc.in.th" class="hover:underline">จองคิว</a>
        </li>
      </ul>
    </div>
  {/if}

  <div class="min-h-screen font-extralight">
    <header class="border-[0.5px] border-white">
      <nav class="flex sm:hidden justify-end space-x-4 px-6 py-2">
        <button
          on:click={handleClick}
          class="border border-white rounded-md px-1 py-1"
        >
          <svg
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M4 6H20M4 12H20M4 18H20"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </button>
      </nav>

      <nav class="hidden sm:flex justify-end space-x-4 px-6 py-4">
        <ul class="flex space-x-4">
          <li class="">
            <a href="http://12.jwc.in.th" class="hover:underline"
              >เกี่ยวกับหมอหมึก</a
            >
          </li>
          <li class="">
            <a href="http://12.jwc.in.th" class="hover:underline">บทความ</a>
          </li>
          <li class="">
            <a href="http://12.jwc.in.th" class="hover:underline">จองคิว</a>
          </li>
        </ul>
      </nav>
    </header>

    <main class="text-center pt-16 pb-8 space-y-5 px-4 text-lg sm:text-xl">
      <h1 class="font-base text-5xl sm:text-6xl">หมอหมึก</h1>
      <p>ผู้มีประสบการณ์พยากรณ์มากกว่า 10 ปี<br />พร้อมคำพยากรณ์ที่แม่นยำ</p>

      <a
        href="https://12.jwc.in.th"
        class="inline-block text-[#612378] py-3 px-10 transition-all hover:scale-105 hover:bg-gray-100 bg-white"
      >
        จองคิว
      </a>
    </main>

    <section
      class="px-6 md:max-w-3xl lg:max-w-4xl mx-auto py-8 flex flex-col-reverse items-center sm:flex-row gap-6"
    >
      <div class="flex flex-col mx-4">
        <h2 class="font-base text-3xl mt-3 mb-3">ประวัติหมอหมึก</h2>
        <p class="mb-4">
          หมอหมึกเป็นนักพยากรณ์ที่ชำนาญการด้านการทำนายดวงด้วยลูกแก้วพยากรณ์
          ไพ่ทาโรต์ และการดูลายมือ
        </p>
        <p>
          ด้วยความสามารถที่หลากหลาย
          ทำให้หมอหมึกสามารถเลือกวิธีการทำนายที่เหมาะกับแต่ละบุคคลเพื่อให้ได้ผลลัพธ์แม่นยำที่สุด
        </p>
      </div>

      <div class="flex">
        <img
          class="border border-white"
          alt="หมอหมึก"
          src="/assets/หมอหมึก.jpg"
        />
      </div>
    </section>

    <section class="py-8 px-4">
      <h2 class="font-base text-3xl mb-10 text-center">รีวิวจากลูกค้า</h2>

      <article
        class="grid grid-cols-1 sm:grid-cols-3 max-w-[14rem] sm:max-w-xl gap-6 lg:max-w-4xl mx-auto"
      >
        <div class="flex text-center flex-col justify-center items-center">
          <img
            class="border border-white h-[150px] w-[150px] object-cover rounded-full aspect-square"
            alt="แมทธิว"
            src="/assets/นักธุรกิจ.jpg"
          />

          <h3 class="mt-6 mb-3 text-2xl font-base">แมทธิว นักธุรกิจ</h3>

          <p>
            หมอหมึกช่วยผมเรื่องฤกษ์ยามใน การเจรจาธุรกิจได้มากเลย
            ตอนนี้ขายดีเทน้ำเทท่าเลยครับ
          </p>
        </div>

        <div class="flex text-center flex-col justify-center items-center">
          <img
            class="border h-[150px] w-[150px] object-cover border-white rounded-full aspect-square"
            alt="แจ็ค"
            src="/assets/นักแสดง.jpg"
          />

          <h3 class="mt-6 mb-3 text-2xl font-base">แจ็ค นักแสดง</h3>

          <p>
            ต้องขอขอบคุณหมอหมึกในการช่วยให้ความ สัมพันธ์ราบรื่นนะคะ
            ทำนายอะไรไว้ก็แม่นทุกอย่างเลยค่ะ
          </p>
        </div>

        <div class="flex text-center flex-col justify-center items-center">
          <img
            class="border h-[150px] w-[150px] object-cover border-white rounded-full aspect-square"
            alt="น้ำใส"
            src="/assets/นักศึกษา.jpg"
          />

          <h3 class="mt-6 mb-3 text-2xl font-base">น้ำใส นักศึกษา</h3>

          <p>
            ที่หมอหมึกบอกมานะคะ เกิดเกือบหมดเลยค่ะ ถ้าไม่ได้หมอหมึกช่วยไว้
            ชีวิตคงแย่เลยค่ะ ดีนะที่ป้องกันเรื่องร้าย ๆ ทันเวลา
          </p>
        </div>
      </article>
    </section>

    <section
      class="grid grid-cols-1 sm:grid-cols-2 gap-4 py-8 px-4 md:max-w-3xl lg:max-w-4xl mx-auto"
    >
      <div>
        <h2 class="font-base text-3xl mb-10">ทำนายชะตากับหมอหมึก</h2>

        <p>
          สามารถจองคิวได้บนเว็บไซต์ หรือ
          <br />
          อีเมล​ : octopus_fortune@teller.com
          <br />
          โทรศัพท์ : 099 XXX XXXX
          <br />
          และมาที่สำนักที่
        </p>

        <p>
          ชั้น 12 อาคาร JWC ถนนโปรแกรมมิ่ง แขวงเว็บ เขตอินเตอร์เน็ต กรุงเทพฯ
          99999
        </p>

        <p>ตามวันและเวลาที่นัดไว้</p>

        <p class="mt-6">
          จำกัดที่ 10 คิวต่อหนึ่งวัน เปิดทำการ 10.00-18.30 น. พัก 12.00-13.00 น.
          <br />
          เปิดทุกวันอังคารถึงเสาร์ หยุดวันจันทร์และอาทิตย์
        </p>
      </div>

      <iframe
        class="border w-full border-white"
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3875.792645053!2d100.7811136!3d13.731000199999999!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x311d66308ce98ffd%3A0xcb43a76f038c38ca!2sFaculty%20of%20Infomation%20Technology!5e0!3m2!1sen!2sth!4v1655493002737!5m2!1sen!2sth"
        width="600"
        height="450"
        style="border:0;"
        allowfullscreen
        title="สถานที่"
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
      />
    </section>
  </div>
</body>

<style>
  body {
    font-family: "Pridi", serif;
  }
</style>
