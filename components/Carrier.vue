
<template>

  <div class="car">
      {{item}} sss<br />
      {{header}} header<br />
      {{carrier.year}}年{{carrier.desc}} cal
    </div>

</template>

<script>
export default {
  name: 'item',
  props: ['item','header','data','carrier'],
  data () {
    return {}
  }
}
</script>
<style>
.car {
  font-size: 20px;
}

.carrier,
.carrier th,
td {
  border: solid 1px black;
  border-spacing: 0;
  border-collapse: collapse;
}

</style>
