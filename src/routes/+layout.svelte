<script>
  import "../app.css";
  /**@type {}*/
  let model;
  const openModel = () => {
    if (model) {
      model.showModal();
    }
  };
</script>

<div class="w-full bg-base-200">
  <div class="navbar max-w-6xl mx-auto">
    <div class="flex">
      <a class="text-xl cursor-pointer font-bold text-primary">SHORT URL</a>
    </div>
    <div class="flex-1 flex justify-center">
      <!-- <a class="btn btn-ghost text-xl">Home</a>
      <a class="btn btn-ghost text-xl">My Links</a> -->
    </div>
    <button class="btn btn-ghost text-xl" on:click={openModel}>Login</button>
  </div>
</div>

<dialog bind:this={model} id="my_modal_2" class="modal">
  <div class="modal-box flex flex-col gap-3 p-5 bg-base-200 rounded-lg">
    <input class="input" placeholder="Email" />
    <input class="input" placeholder="Password" type="password" />
    <button class="btn btn-primary">Login</button>
    <div class="divider">OR</div>
    <button class="btn btn-neutral">
      Login with google
      <img class="w-[40px] h-[40px]" src="googleLogo.png" />
    </button>
  </div>
  <form method="dialog" class="modal-backdrop">
    <button>close</button>
  </form>
</dialog>
<div class="container w-full max-w-3xl mx-auto">
  <slot />
</div>
