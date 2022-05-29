<script lang="ts">
  import Icon from '@iconify/svelte';

  function Age() {
    var dob = new Date('09/05/2006');
    var month_diff = Date.now() - dob.getTime();
    var age_dt = new Date(month_diff);
    var year = age_dt.getUTCFullYear();
    var age = Math.abs(year - 1970);
    return age;
  }
</script>

<svelte:head>
  <title>Mazylol</title>
  <meta name="description" content="Svelte Magic!!!" />
</svelte:head>

<div class="min-h-screen bg-zinc-800">
  <p class="text-center text-5xl text-gray-300 p-5">
    My age: <span
      class="px-2 py-1 font-extrabold bg-gradient-to-r from-orange-500 to-red-700 rounded-md"
    >
      {Age()}
    </span>
  </p>
  <Icon icon="ant-design:heart-filled" class="text-red-500 mx-auto text-6xl" />
</div>
