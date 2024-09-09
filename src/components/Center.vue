<template>
  <div class="container">
    <div class="content">
      <div class="left-side">
        <img src="@/assets/4447.jpg" alt="Sample Image" />
      </div>
      <div class="right-side">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas
          condimentum mauris at elit aliquet, nec commodo urna facilisis.
          Curabitur et libero eget nulla dictum fringilla et et sapien. Sed
          ultricies, lacus a feugiat faucibus, nisi ipsum cursus arcu, a dapibus
          purus libero vitae tortor.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BodyComponent",
};
</script>

<style scoped>
.container {
  width: 100%;
  display: flex;
  justify-content: center;
}

.content {
  display: flex;
  max-width: 1200px;
  width: 100%;
  flex-wrap: nowrap;
  padding: 20px;
}

.left-side {
  flex: 3; /* 60% of the space */
}

.right-side {
  flex: 2; /* 40% of the space */
  padding-left: 20px;
  display: flex;
  justify-content: center;
  align-items: center; /* Vertically center the content */
}

.left-side img {
  width: 100%;
  height: auto; /* Maintain aspect ratio */
}

.right-side p {
  text-align: justify;
}

@media (max-width: 768px) {
  .content {
    flex-direction: column;
    align-items: center;
  }

  .left-side,
  .right-side {
    width: 100%; /* Full width on mobile */
  }

  .right-side {
    padding-left: 0;
    padding-top: 20px;
    display: block; /* Reset the flexbox on mobile */
  }
}
</style>
