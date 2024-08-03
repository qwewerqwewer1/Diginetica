<template>
	<div class="range">
		<h2 class="range__head">Цена</h2>

		<div class="range__fields">
			<label class="range__field">
				<span class="range__title">от</span>
				<input
					type="number"
					name="price-from"
					placeholder="5500 ₽"
					min="0"
					max="10000"
					step="100"
					class="range__input"
				/>
			</label>

			<span class="range__separator"></span>

			<label class="range__field">
				<span class="range__title">до</span>
				<input
					type="number"
					name="price-to"
					placeholder="5500 ₽"
					min="0"
					max="10000"
					step="100"
					class="range__input"
				/>
			</label>
		</div>
	</div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.range {
	display: flex;
	flex-direction: column;
	gap: 16px;

	&__head {
		color: var(--light-dark);
		font-size: 16px;
		line-height: 20px;
		font-weight: 700;
		text-align: center;
	}

	&__fields {
		display: grid;
		grid-template-columns: 1fr 10px 1fr;
		align-items: center;
		gap: 16px;
	}

	&__field {
		display: flex;
		align-items: center;
		gap: 6px;
		padding: 10px 8px;

		border: 1px solid var(--color-border);
		background-color: var(--white);
		border-radius: 4px;
	}

	&__title {
		color: var(--light-gray);
		font-size: 12px;
		line-height: 14px;
	}

	&__input {
		background-color: transparent;
		border: none;
		appearance: textfield;

		&::-webkit-outer-spin-button,
		&::-webkit-inner-spin-button {
			appearance: none;
			margin: 0;
		}
	}

	&__separator {
		display: flex;
		justify-content: center;
		align-items: center;

		width: 10px;
		height: 1px;
		background-color: var(--color-border);
	}
}
</style>
