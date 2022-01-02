<script>
    import {page} from "$app/stores";

    let name="";
    $:name=page.params
</script>

<p>{name}</p>
<a href="/tab/1">1</a>
<a href="/tab/2">2</a>
<a href="/tab/3">3</a>
