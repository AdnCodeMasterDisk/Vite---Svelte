<script>
    import {Router,Link,Route,createMemorySource,createHistory,} 
    from "svelte-navigator";
    import homeView from "../views/home.svelte";
    import aboutView from "../views/about.svelte";

    const history = createHistory(createMemorySource());
</script>


<Router {history}>

    <div class="menu">
        <Link class="itemMenu" to="/">Home</Link>
        <Link class="itemMenu" to="about">About</Link>
    </div>

    <main>
        <Route path="/" component="{homeView}" />
        <Route path="about" component="{aboutView}" />
    </main>
</Router>