<template>
  <div class="w-full flex justify-center items-center h-screen">
    <form
      action="https://send.pageclip.co/0U0AWb8kRSVXQPuIRWiYVVJkLUjFE7QI/contact-form"
      class="pageclip-form relative w-2/5 flex flex-col items-start space-y-4"
      method="post"
    >
      <div class="w-full flex space-x-4">
        <div class="w-1/2">
          <label for="name">
            <span class="font-normal text-red-500">*</span> Nombre y Apellidos:
          </label>
          <input
            id="name"
            type="text"
            name="name"
            placeholder="Lucas Galípolo"
            required
          />
        </div>
        <div class="w-1/2">
          <label for="email">
            <span class="font-normal text-red-500">*</span> Email:
          </label>
          <input
            id="email"
            type="email"
            name="email"
            placeholder="lucas@galipolo.me"
            required
          />
        </div>
      </div>
      <div class="w-full">
        <label for="subject">
          <span class="font-normal text-red-500">*</span> Asunto:
        </label>
        <input
          id="subject"
          type="text"
          name="subject"
          placeholder="Comprar patatas ;D"
          required
        />
      </div>

      <div class="w-full">
        <label for="content">
          <span class="font-normal text-red-500">*</span> Contenido del mensaje:
        </label>
        <textarea
          id="content"
          name="content"
          cols="30"
          rows="10"
          class="w-full"
        ></textarea>
      </div>

      <button
        class="
          pageclip-form__submit
          button
          relative
          w-1/4
          px-4
          py-2
          bg-purple-500
          rounded-md
          hover:bg-purple-600
          active:bg-purple-700
          text-white
          font-semibold
          shadow-sm
          active:ring active:ring-purple-400
          focus:outline-none
        "
        type="submit"
      >
        <span>Enviar</span>
      </button>
    </form>
  </div>
</template>

<style scoped>
input,
textarea {
  @apply w-full rounded-md mt-2 dark:bg-gray-300 dark:placeholder-gray-600;
}

label {
  @apply font-semibold dark:text-gray-200;
}
</style>
