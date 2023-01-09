<script>
    import "../app.css"
    import Nav from "../components/nav.svelte"
    import '../lib/assets/css/nucleo-icons.css';

</script>

<div class="p-8 max-w-6xl mx-auto">
    <Nav/>

	<div class="leading-normal text-center text-sm text-slate-500 mt-3">
		© made with ♥️<i class="fa fa-heart" /> by
		<a
			href="https://www.sixsigma.com.br"
			class="font-semibold text-red-900"
			target="_blank"
			rel="noreferrer">Sixsigma Technologies</a
		>
	</div>

	

    <div class="leading-normal text-center text-sm text-slate-500 lg:text-center m-3">
        © made with <i class="ni leading-none ni-favourite-28 text-lg relative top-0.3 text-red-700" /> by
        <a
            href="https://www.sixsigma.com.br"
            class="font-semibold text-red-900"
            target="_blank"
            rel="noreferrer">Sixsigma</a
        >
    </div>

    <slot></slot>
</div>
