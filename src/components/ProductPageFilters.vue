<template>
	<div class="filters">
		<FiltersCategory />

		<FiltersPrice />

		<FiltersBrand />

		<FiltersSize />
	</div>
</template>

<script>
import FiltersCategory from "./ProductPageFiltersCategory";
import FiltersPrice from "./ProductPageFiltersPrice";
import FiltersBrand from "./ProductPageFiltersBrand";

import FiltersSize from "./ProductPageFiltersSize";
export default {
	components: {
		FiltersCategory,
		FiltersPrice,
		FiltersBrand,
		FiltersSize,
	},
	data() {
		return {};
	},
};
</script>

<style lang="scss" scoped>
.filters {
	display: flex;
	flex-direction: column;
	gap: 28px;
}
</style>
