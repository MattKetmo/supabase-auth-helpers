<script lang="ts">
	export let errors: Record<string, string> = null;
	export let values: Record<string, string> = null;
</script>

<section class="columns mt-6 pt-6">
	<div class="column is-half is-offset-one-quarter">
		<h1 class="title">Sign in</h1>
		{#if errors}
			<div class="block notification is-danger">{errors.form}</div>
		{/if}
		<form method="post">
			<div class="field">
				<label for="email" class="label">Email</label>
				<p class="control">
					<input
						id="email"
						name="email"
						value={values?.email ?? ''}
						class="input"
						type="email"
						placeholder="Email"
						required
					/>
				</p>
			</div>
			<div class="field">
				<label for="password" class="label">Password</label>
				<p class="control">
					<input
						id="password"
						name="password"
						value={values?.password ?? ''}
						class="input"
						type="password"
						placeholder="Password"
						required
					/>
				</p>
			</div>
			<div class="field">
				<p class="control">
					<button class="button is-fullwidth is-link">Sign in</button>
				</p>
			</div>
		</form>

		<div class="mt-6">
			<p class="has-text-centered">
				Don't have an account? <a href="/signup">Sign up</a>
			</p>
		</div>
	</div>
</section>
