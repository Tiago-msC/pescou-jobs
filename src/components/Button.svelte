<script lang="ts">
  export let text: string = "";
  export let expended: boolean = false;
  export let iconLeft: string = "";
  export let iconLeftAlt: string = "";
  export let iconRight: string = "";
  export let iconRightAlt: string = "";
  export let type: "primary" | "outline" = "primary";
  export let fontSize: string = "0.9rem";
  export let disabled: boolean = false;
  export let processing: boolean = false;
  export let notClickAnimation: boolean = false;
  export let onClick: () => void = () => {};

  let isProcessing: boolean = false;

  function handleClick() {
    if (disabled || isProcessing) {
      return;
    }

    onClick();
    if (processing) {
      isProcessing = true;
      setTimeout(() => {
        isProcessing = false;
      }, 1000);
    }
  }

  function handleKeyDown(event: KeyboardEvent) {
    if (event.key === "Enter" || event.key === " ") {
      handleClick();
    }
  }
</script>

<div
  class:expended
  class:disabled
  class:primary={type === "primary"}
  class:outline={type === "outline"}
  class:loading={isProcessing}
  class:notClickAnimation
  on:click={handleClick}
  on:keydown={handleKeyDown}
  tabindex={disabled ? -1 : 0}
  role="button"
  aria-disabled={disabled}
  style="height: calc({fontSize} + 30px);"
>
  {#if iconLeft}
    <img class="icon-left" src={iconLeft} alt={iconLeftAlt} />
  {/if}

  {#if isProcessing && processing}
    <span
      class="spinner"
      style="width: calc({fontSize} + 0.65em); height: calc({fontSize} + 0.65em; filter: invert({type ===
      'primary'
        ? 1
        : 0});"
    />
  {:else if text}
    <span style="font-size: {fontSize};">{text}</span>
  {/if}

  {#if iconRight}
    <img class="icon-right" src={iconRight} alt={iconRightAlt} />
  {/if}
</div>

<style>
  div {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 10px 16px;
    width: fit-content;
    cursor: pointer;
  }

  .primary {
    background-color: var(--theme-text-color-primary);
  }

  .primary:hover:not(.disabled):not(.loading) {
    background-color: var(--theme-button-hove-color-primary);
  }

  .primary:active:not(.disabled):not(.loading):not(.notClickAnimation), .outline:active:not(.disabled):not(.loading):not(.notClickAnimation) {
    transform: scale(0.98);
    transition: transform 0.1s ease-in-out;
  }

  .outline {
    border: 1px solid var(--theme-border-color-secondary);
  }

  .outline:hover:not(.disabled):not(.loading) {
    background-color: var(--theme-button-hove-color-outline);
  }

  .outline > span {
    color: var(--theme-border-color-secondary);
  }

  .disabled {
    cursor: not-allowed;
  }

  .primary.disabled {
    background-color: var(--theme-button-hove-color-primary);
  }

  .outline.disabled {
    border: 1.5px solid var(--theme-button-hove-color-outline-disabled);
  }

  .outline.disabled > span {
    color: var(--theme-text-color-secondary);
  }

  .outline.disabled > img {
    filter: invert(0.5);
  }

  .icon-left {
    margin-right: 8px;
  }

  .icon-right {
    margin-left: 8px;
  }

  .expended {
    width: auto;
  }

  span {
    color: var(--theme-text-color-tertiary);
    font-family: var(--theme-typography-font-family-semibold);
    font-size: 0.8rem;
    margin: 0 auto;
  }

  .spinner {
    background: transparent;
    box-sizing: border-box;
    border-top: 3px solid var(--theme-text-color-primary);
    border-left: 3px solid transparent;
    border-right: 3px solid transparent;
    border-bottom: 3px solid transparent;
    border-radius: 100%;
    animation: spin 0.6s ease-out infinite;
  }
  @keyframes spin {
    100% {
      transform: rotate(360deg);
    }
  }

  .loading {
    pointer-events: stroke;
  }
</style>
