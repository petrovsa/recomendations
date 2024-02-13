<template>
    <svg v-if="name === 'arrow'" width="27" height="18" viewBox="0 0 27 18" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M9.52778 17L1.75 9M1.75 9L9.52778 1M1.75 9H25.75" stroke="black" stroke-width="2" stroke-linecap="round"
            stroke-linejoin="round" />
    </svg>
    <svg v-else-if="name === 'star'" width="16" height="16" viewBox="0 0 16 16" fill="none"
        xmlns="http://www.w3.org/2000/svg">
        <path
            d="M15.352 5.8632L10.7407 5.15883L8.67384 0.756328C8.51947 0.427578 7.98009 0.427578 7.82572 0.756328L5.75947 5.15883L1.14822 5.8632C0.769468 5.92133 0.618218 6.38195 0.883843 6.65383L4.23384 10.0876L3.44197 14.942C3.37884 15.3276 3.79072 15.617 4.13134 15.4276L8.25009 13.1513L12.3688 15.4282C12.7063 15.6157 13.122 15.332 13.0582 14.9426L12.2663 10.0882L15.6163 6.65445C15.882 6.38195 15.7301 5.92133 15.352 5.8632Z"
            fill="#F5793B" />
    </svg>
    <svg v-else-if="name === 'star-grey'" width="16" height="16" viewBox="0 0 16 16" fill="none"
        xmlns="http://www.w3.org/2000/svg">
        <path
            d="M10.175 5.42444L10.3167 5.72631L10.6463 5.77666L14.9571 6.43514L11.819 9.65175L11.5987 9.87752L11.6495 10.1888L12.3895 14.7255L8.55247 12.6043L8.25013 12.4372L7.94778 12.6043L4.11063 14.7249L4.85069 10.1882L4.90147 9.8769L4.68121 9.65113L1.54358 6.43506L5.85384 5.77666L6.18355 5.7263L6.32525 5.42437L8.2498 1.32379L10.175 5.42444Z"
            fill="#E5E3D4" stroke="#E5E3D4" stroke-width="1.25" />
    </svg>
</template>

<script>
export default {
    props: ['name']
}
</script>