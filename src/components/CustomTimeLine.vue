<template>
  <div class="timeline-wrapper">
    <ul class="StepProgress">
      <li class="StepProgress-item is-done">
        <div class="bold">Step 1</div>
      </li>
      <li class="StepProgress-item is-done">
        <div class="bold">Step 2</div>
        <div>Post a contest</div>
      </li>
      <li class="StepProgress-item current">
        <div class="bold">Step 3</div>
      </li>
      <li class="StepProgress-item">
        <div class="bold">Step 4</div>
      </li>
      <li class="StepProgress-item">
        <div class="bold">Step 5</div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style>
.bold {
  font-weight: bold;
}
.timeline-wrapper {
  padding-left: 80px;
  min-width: 400px;
  font-family: "Helvetica";
  font-size: 14px;
  /*border: 1px solid #CCC;*/
}
.StepProgress {
  position: relative;
  padding-left: 45px;
  list-style: none;
}
.StepProgress::before {
  display: inline-block;
  content: "";
  position: absolute;
  top: 0;
  left: 15px;
  width: 10px;
  height: 100%;
  border-left: 2px solid #ccc;
}
.StepProgress-item {
  position: relative;
  counter-increment: list;
}
.StepProgress-item:not(:last-child) {
  padding-bottom: 20px;
}
.StepProgress-item::before {
  display: inline-block;
  content: "";
  position: absolute;
  left: -30px;
  height: 100%;
  width: 10px;
}
.StepProgress-item::after {
  content: "";
  display: inline-block;
  position: absolute;
  top: 0;
  left: -37px;
  width: 12px;
  height: 12px;
  border: 2px solid #ccc;
  border-radius: 50%;
  background-color: #fff;
}
.StepProgress-item.is-done::before {
  border-left: 2px solid green;
}
.StepProgress-item.is-done::after {
  /*content: "?";*/
  font-size: 10px;
  color: #fff;
  text-align: center;
  border: 2px solid green;
  background-color: green;
}
/*.StepProgress-item.current::before { 
border-left: 2px solid green;
}
.StepProgress-item.current::after {
content: counter(list);
padding-top: 1px;
width: 19px;
height: 18px;
top: -4px;
left: -40px;
font-size: 14px;
text-align: center;
color: green;
border: 2px solid green;
background-color: white;
}*/
.StepProgress strong {
  display: block;
}
</style>
