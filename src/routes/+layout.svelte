<script>
    import '../app.css';
    import Footer from './footer.svelte';
    import Header from './header.svelte';
    import PageTransition from './transition.svelte';

    let {children, data} = $props();
</script>

<div class="contain-layout max-w-screen-lg m-auto">
    <Header/>
    <main>
        <PageTransition url={data.url}>
            {@render children?.()}
        </PageTransition>
    </main>
    <Footer/>
</div>
