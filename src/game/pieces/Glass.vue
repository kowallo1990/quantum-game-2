<template>
	<svg>
		<g>
			<g>
				<g class="st0">
					<path
						class="st1"
						d="M52.6,56.7c1.8-1,3.2-2.4,4.2-4.2c-1,0.5-2,0.9-3.1,1.1C53.5,54.8,53.1,55.8,52.6,56.7z"
					/>
				</g>
				<g class="st0">
					<path
						class="st1"
						d="M11.4,7.3c-1.8,1-3.2,2.4-4.2,4.2c0.9-0.5,2-0.9,3.1-1.1C10.5,9.2,10.9,8.2,11.4,7.3z"
					/>
				</g>
				<g>
					<path
						class="st1"
						d="M58,16.4C58,10.7,53.3,6,47.6,6H16.4c-1.8,0-3.5,0.5-5,1.3c-0.5,1-0.9,2-1.1,3.1c0.6-0.1,1.2-0.2,1.9-0.2
						h31.2c5.7,0,10.4,4.7,10.4,10.4v31.2c0,0.7-0.1,1.3-0.2,1.9c1.1-0.2,2.1-0.6,3.1-1.1c0.8-1.5,1.2-3.2,1.2-5V16.4z"
					/>
				</g>
				<g class="st2">
					<path
						class="st1"
						d="M51.8,53.8H20.6c-5.7,0-10.4-4.7-10.4-10.4V12.2c0-0.6,0.1-1.3,0.2-1.9c-1.1,0.2-2.1,0.6-3.1,1.1
						c-0.8,1.5-1.3,3.2-1.3,5v31.2C6,53.3,10.7,58,16.4,58h31.2c1.8,0,3.5-0.5,5-1.3c0.5-1,0.9-2,1.1-3.1C53,53.8,52.4,53.8,51.8,53.8
						z"
					/>
				</g>
				<g class="st0">
					<path
						class="st1"
						d="M9.8,43.6c0,5.8,4.7,10.6,10.6,10.6h31.7c0.7,0,1.3-0.1,1.9-0.2c0.1-0.6,0.2-1.3,0.2-1.9V20.4
						c0-5.8-4.7-10.6-10.6-10.6H11.9c-0.7,0-1.3,0.1-1.9,0.2c-0.1,0.6-0.2,1.3-0.2,1.9C9.8,11.9,9.8,43.6,9.8,43.6z"
					/>
				</g>
			</g>
			<path
				class="st3"
				d="M47.6,6H16.4c-1.2,0-2.3,0.2-3.4,0.6c3.4,9.3,12.5,28.9,34.5,51.4h0.1C53.3,58,58,53.3,58,47.6V16.4
				C58,10.7,53.3,6,47.6,6z"
			/>
			<path class="st3" d="M47.6,6H28.3c4.6,6.9,13.8,18.6,29.7,28.9V16.4C58,10.7,53.3,6,47.6,6z" />
		</g>
		<g v-if="border" id="_x3C_Qoutline_x3E_">
			<path
				class="st4"
				:style="{ fill: border }"
				d="M47.6,6C53.3,6,58,10.7,58,16.4v31.2C58,53.3,53.3,58,47.6,58H16.4C10.7,58,6,53.3,6,47.6V16.4
				C6,10.7,10.7,6,16.4,6H47.6 M47.6,5H16.4C10.1,5,5,10.1,5,16.4v31.2C5,53.9,10.1,59,16.4,59h31.2C53.9,59,59,53.9,59,47.6V16.4
				C59,10.1,53.9,5,47.6,5L47.6,5z"
			/>
		</g>
	</svg>
</template>

<script lang="ts">
import { Component } from 'vue-property-decorator';
import Piece from './Piece';

@Component
export default class Glass extends Piece {}
</script>

<style lang="scss" scoped>
.st0 {
	opacity: 0.66;
}
.st1 {
	fill: #61dbef;
}
.st2 {
	opacity: 0.82;
}
.st3 {
	opacity: 0.15;
	fill: #ffffff;
}
</style>
