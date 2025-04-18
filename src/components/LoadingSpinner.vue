<template>
    <div class="flex justify-center items-center w-full h-screen bg-blue-hue">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 150 75" width="75" height="37.5">
        <path
          fill="none"
          stroke="#0CA7FF"
          stroke-width="10"
          stroke-linecap="round"
          stroke-dasharray="100 192.5"
          stroke-dashoffset="0"
          d="M137.5 37.5c0 15.5-13.5 25-25 25-29 0-46-50-75-50-14 0-25 11-25 25s12 25 25 25c29 0 46-50 75-50 12 0 25 9.5 25 25Z"
        >
          <animate
            attributeName="stroke-dashoffset"
            calcMode="spline"
            dur="2s"
            values="342.5;0"
            keySplines="0 0 1 1"
            repeatCount="indefinite"
          />
        </path>
      </svg>
    </div>
  </template>
  
  <script>
  export default {};
  </script>
  
  <style>
  
  </style>