<script lang="ts">
    export let pageTitle: string = "";
    export let description: string = "";
</script>

<div>
    <h1 class="font-semibold">
        {pageTitle}
    </h1>
    <p class="text-muted-foreground">
        {description}
    </p>
</div>