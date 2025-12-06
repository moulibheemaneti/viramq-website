<template>
   <div class="vq-layout">

      <header class="vq-header--error">
         <VqLogo height="48" />
      </header>

      <main class="vq-main">
         <h1 class="vq-error-title">Oops! Something went wrong.</h1>
         <p class="vq-error-message">
            We couldn't find the page you were looking for.
         </p>
         <p class="vq-error-message">It might have been moved or doesn't exist.</p>
         <NuxtLink to="/" class="vq-button">Go to Home Page</NuxtLink>
      </main>

      <VqFooter />

      <VqFooterDecorator />
   </div>
</template>


<style scoped lang="scss">
.vq-layout {
   display: flex;
   min-height: 100vh;
   flex-direction: column;
}

.vq-header--error {
   display: flex;
   align-items: center;
   padding: 2rem 0 1rem 0;
   justify-content: center;
}

.vq-main {
   flex: 1;
   display: flex;
   flex-direction: column;
   align-items: center;
   justify-content: center;
   text-align: center;
   padding-bottom: 2rem;
}

.vq-error-title {
   font-size: 2.2rem;
   font-weight: 700;
   margin-bottom: 1.2rem;
   color: #f5f0bb;
}

.vq-error-message {
   font-size: 1.15rem;
   color: #f5f0bba5;

   &:nth-child(3) {
      margin-bottom: 2rem;
   }
}

.vq-home-btn {
   display: inline-block;
   padding: 0.7rem 1.8rem;
   background: #73a9ad;
   color: #212529;
   border-radius: 8px;
   font-size: 1rem;
   font-weight: 600;
   letter-spacing: 0.02em;
   text-decoration: none;
   transition: background 0.2s;
   box-shadow: 0 2px 8px #0002;
}

.vq-home-btn:hover {
   background: #5c8588;
   color: #fff;
}
</style>
