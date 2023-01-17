<script>
    export let config = {};

    const defaults = {
        name: "program",
        width: 400,
        height: 400,
        script: function(canvas, context){},
    }

    config = Object.assign(Object.create(defaults), config);
</script>

<style>
    canvas {
        max-width: min(width, height);
        max-height: min(width, height);
    }
</style>

<canvas width={config.width} height={config.height}>
    {config.name}, an interactive canvas.
</canvas>
