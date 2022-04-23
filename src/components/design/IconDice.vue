<template>
  <span class="dice-icon">
    <svg width="24" height="24" xmlns="http://www.w3.org/2000/svg">
      <path
        d="M20 0H4a4.005 4.005 0 0 0-4 4v16a4.005 4.005 0 0 0 4 4h16a4.005 4.005 0 0 0 4-4V4a4.005 4.005 0 0 0-4-4ZM7.5 18a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3Zm0-9a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3Zm4.5 4.5a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3Zm4.5 4.5a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3Zm0-9a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3Z"
        fill="#1f2732"
      />
    </svg>
  </span>
</template>

<style scoped>
.dice-icon {
  padding: 20px;
  border-radius: 100%;
  background-color: #52ffa8;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}

.dice-icon:hover {
  box-shadow: 0 0 30px 5px #52ffa8;
}

.dice-icon svg {
  display: inline-block;
  vertical-align: middle;
}
</style>