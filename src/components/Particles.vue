<script setup>
const particlesLoaded = async container => {
    console.log("Particles container loaded", container);
};
</script>
<template>
    <div id="particles-js">
        <vue-particles id="tsparticles" @particles-loaded="particlesLoaded" />
        <div></div>
        <vue-particles
            id="tsparticles"
            @particles-loaded="particlesLoaded"
            :options="{
                autoPaly: true,
                pauseOnBlur: true,
                pauseOnOutsideViewport: true,
                background: {
                    color: {
                        value: '#455A64'
                    }
                },
                backgroundMask: {
                    composite: 'destination-out'
                },
                fullScreen: {
                    enable: true,
                    zIndex: -1
                },
                fpsLimit: 120,
                interactivity: {
                    events: {
                        onClick: {
                            enable: true,
                            mode: 'repulse'
                        },
                        onHover: {
                            enable: true,
                            mode: 'grab',
                            parallax: {
                                enable: true,
                                force: 15,
                                smooth: 100
                            }
                        }
                    },
                    modes: {
                        bubble: {
                            distance: 400,
                            duration: 2,
                            opacity: 0.8,
                            size: 40
                        },
                        push: {
                            quantity: 2
                        },
                        repulse: {
                            distance: 200,
                            duration: 0.8
                        },
                        attract: {
                            distance: 180,
                            duration: 5,
                            easing: 'ease-out-quad',
                            factor: 5,
                            maxSpeed: 10,
                            speed: 3
                        },
                        grab: {
                            distance: 230
                        }
                    }
                },
                particles: {
                    color: {
                        value: '#e65757ff',
                        animation: {
                            h: {
                                enable: true,
                                speed: 20,
                                sync: true
                            }
                        }
                    },
                    links: {
                        color: '#ffffff',
                        distance: 150,
                        enable: true,
                        opacity: 0.4,
                        width: 1
                    },
                    move: {
                        direction: 'none',
                        enable: true,
                        outModes: 'bounce',
                        random: true,
                        speed: 6,
                        straight: false
                    },
                    number: {
                        density: {
                            enable: true
                        },
                        value: 250
                    },
                    opacity: {
                        value: 0.5
                    },
                    shape: {
                        type: 'circle'
                    },
                    size: {
                        value: { min: 0.5, max: 4 }
                    }
                },
                detectRetina: true
            }"
        />
    </div>
</template>

<style scoped>
.read-the-docs {
    color: #888;
}
</style>
