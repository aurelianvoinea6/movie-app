<script context="module">
	export async function load({ fetch, params }) {
		const res = await fetch(
			`https://api.themoviedb.org/3/movie/${params.id}?api_key=f3146106483004e6072b34c9e290fa28&language=en-US`
		);
		const movieDetail = await res.json();

		if (res.ok) {
			return {
				props: { movieDetail }
			};
		}
	}
</script>
