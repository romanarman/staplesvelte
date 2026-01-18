<script lang="ts">
  export let title: string;
  export let body: string;
</script>

<div class="rounded-3xl border p-6" style="border-color: rgba(37,38,64,0.14);">
  <div class="flex items-start justify-between gap-6">
    <div>
      <div class="text-base font-medium">{title}</div>
      <div class="mt-2 text-sm opacity-85 leading-relaxed">{body}</div>
    </div>
  </div>
</div>
