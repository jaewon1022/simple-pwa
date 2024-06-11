<script>
  import ColorPicker from 'svelte-awesome-color-picker';

  let rgb = { r: 246, g: 240, b: 220, a: 1 };

  let color;
</script>

<div class="main">
  <div>
    <div class="body">
      <div>
        <ColorPicker
          bind:rgb
          bind:color
          isAlpha={false}
          isTextInput={false}
          on:input={({ detail }) => {}}
        />
      </div>
    </div>
  </div>
</div>

<style>
  .main {
    background-color: white;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 100px;
  }

  svg {
    width: 100%;
    height: 100%;
  }

  .body {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
</style>
