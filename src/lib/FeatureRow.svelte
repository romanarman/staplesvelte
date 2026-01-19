<script lang="ts">
  export let title: string;
  export let body: string;

  // Map titles to icons in /static/ingredients/
  const iconFor = (t: string) => {
    const key = t.trim().toLowerCase();
    if (key.includes("bread") || key.includes("sourdough")) return "/ingredients/sourdough.svg";
    if (key.includes("pastry")) return "/ingredients/pastry.svg";
    if (key.includes("coffee")) return "/ingredients/coffee.svg";
    return "";
  };
</script>

<div
  class="rounded-3xl border p-6 transition hover:shadow-sm"
  style="border-color: rgba(37,38,64,0.14);"
>
  <div class="flex items-start gap-5">
    {#if iconFor(title)}
      <div
        class="flex h-16 w-16 shrink-0 items-center justify-center rounded-2xl border"
        style="border-color: rgba(37,38,64,0.14); background-color: rgba(37,38,64,0.03);"
      >
        <img
          src={iconFor(title)}
          alt=""
          class="h-12 w-12 opacity-95"
          loading="lazy"
          aria-hidden="true"
        />
      </div>
    {/if}

    <div class="min-w-0">
      <div class="text-base font-medium tracking-tight">{title}</div>
      <div class="mt-2 text-sm leading-relaxed opacity-85">{body}</div>
    </div>
  </div>
</div>
