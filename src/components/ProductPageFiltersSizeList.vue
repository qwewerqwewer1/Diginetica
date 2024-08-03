<template>
	<ul class="size-list">
		<li class="size-list__item" v-for="size in sizeList" :key="size.id">
			<label class="size-list__control">
				<input
					type="checkbox"
					class="size-list__input visually-hidden"
					:name="size.name"
					:value:="size.value"
				/>
				<span class="size-list__mark"></span>
				<span class="size-list__lead">{{ size.name }}</span>
			</label>

			<span class="quantity">{{ size.quantity }}</span>
		</li>
	</ul>
</template>

<script>
export default {
	props: {
		sizeList: Array,
	},
};
</script>

<style lang="scss" scoped>
.size-list {
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
			.size-list__lead {
				color: var(--provence);
			}
			.size-list__mark {
				border-color: var(--provence);
			}
		}
	}

	&__mark {
		position: absolute;
		width: 20px;
		height: 20px;
		border-radius: 3px;
		border: 1px solid var(--color-border);

		left: 0;
		top: 0px;

		transition: border-color 0.3s ease-in-out;

		&:hover {
			border-color: var(--provence);
		}
	}

	&__input:checked + .size-list__mark::before {
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
