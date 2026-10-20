<script setup lang="ts">
	import { useId } from "vue";

	const clipId = useId();
	const gradientId = useId();
</script>

<template>
	<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
		<g :clip-path="`url(#${clipId})`">
			<circle cx="12" cy="12" r="12" fill="#000000" />
			<path
				d="M7.4 14.85C7.52 14.73 7.68 14.66 7.85 14.66H18.55C18.83 14.66 18.97 15 18.77 15.2L16.6 17.35C16.48 17.47 16.32 17.54 16.15 17.54H5.45C5.17 17.54 5.03 17.2 5.23 17L7.4 14.85Z"
				:fill="`url(#${gradientId})`"
			/>
			<path
				d="M7.4 6.65C7.52 6.53 7.68 6.46 7.85 6.46H18.55C18.83 6.46 18.97 6.8 18.77 7L16.6 9.15C16.48 9.27 16.32 9.34 16.15 9.34H5.45C5.17 9.34 5.03 9 5.23 8.8L7.4 6.65Z"
				:fill="`url(#${gradientId})`"
			/>
			<path
				d="M16.6 10.72C16.48 10.6 16.32 10.53 16.15 10.53H5.45C5.17 10.53 5.03 10.87 5.23 11.07L7.4 13.22C7.52 13.34 7.68 13.41 7.85 13.41H18.55C18.83 13.41 18.97 13.07 18.77 12.87L16.6 10.72Z"
				:fill="`url(#${gradientId})`"
			/>
		</g>
		<defs>
			<linearGradient :id="gradientId" x1="5.45" y1="6.46" x2="18.77" y2="17.54" gradientUnits="userSpaceOnUse">
				<stop stop-color="#9945FF" />
				<stop offset="0.5" stop-color="#14F195" />
				<stop offset="1" stop-color="#00D1FF" />
			</linearGradient>
			<clipPath :id="clipId">
				<rect width="24" height="24" fill="white" />
			</clipPath>
		</defs>
	</svg>
</template>
