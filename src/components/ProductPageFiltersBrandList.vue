<template>
	<ul class="attributes">
		<li class="attributes__item" v-for="brand in brandList" :key="brand.id">
			<label class="attributes__control">
				<input
					:name="brand.name"
					type="checkbox"
					class="attributes__input visually-hidden"
					:value="brand.value"
				/>
				<span class="attributes__mark"></span>
				<span class="attributes__lead">{{ brand.name }}</span>
			</label>

			<span class="quantity">{{ brand.quantity }}</span>
		</li>
	</ul>
</template>

<script>
export default {
	props: {
		brandList: Array,
	},
};
</script>

<style lang="scss" scoped>
.attributes {
	display: flex;
	flex-direction: column;
	gap: 12px;
	height: 268px;
	overflow-y: scroll;

	&::-webkit-scrollbar {
		width: 3px;
	}

	&::-webkit-scrollbar-track {
		background-color: transparent;
	}

	&::-webkit-scrollbar-thumb {
		background-color: var(--color-icons);
		border-radius: 10px;
	}

	&__item {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding-right: 16px;
	}

	&__control {
		position: relative;
		display: block;
		padding-left: 32px;
		cursor: pointer;

		&:hover {
			.attributes__lead {
				color: var(--provence);
			}
			.attributes__mark {
				border-color: var(--provence);
			}
		}
	}

	&__mark {
		position: absolute;
		left: 0;
		top: 0px;

		width: 20px;
		height: 20px;

		border-radius: 3px;
		border: 1px solid var(--color-border);
		transition: border-color 0.3s ease-in-out;

		&:hover {
			border-color: var(--provence);
		}
	}

	&__input:checked + .attributes__mark::before {
		content: "";
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		margin: auto;

		width: 20px;
		height: 20px;
		background-image: url("@/assets/images/filters/checkbox-apply.svg");
		background-repeat: no-repeat;
	}

	&__lead {
		color: var(--light-dark);
		font-size: 14px;
		line-height: 16px;
		transition: color 0.3s ease-in-out;
	}
}
</style>
