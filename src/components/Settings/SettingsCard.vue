<template>
    <div>
        <div class="meme">
            <b-tabs pills >
                <b-tab active>
                <template v-slot:title >
                    <i class="ni ni-cloud-upload-96 mr-2"></i> Home
                </template>
                <p class="p-3">Raw denim you probably haven't heard of them jean shorts Austin. Nesciunt tofu stumptown aliqua, retro synth master cleanse. Mustache cliche tempor, williamsburg carles vegan helvetica. Reprehenderit butcher retro keffiyeh dreamcatcher synth.</p>
                </b-tab>

                <b-tab>
                <template v-slot:title>
                    <i class="ni ni-bell-55 mr-2"></i> Profile
                </template>
                <p class="p-3">Cosby sweater eu banh mi, qui irure terry richardson ex squid. Aliquip placeat salvia cillum iphone. Seitan aliquip quis cardigan american apparel, butcher voluptate nisi qui.</p>
                </b-tab>

                <b-tab>
                <template v-slot:title>
                    <i class="ni ni-calendar-grid-58 mr-2"></i> Messages
                </template>
                <p class="p-3">Raw denim you probably haven't heard of them jean shorts Austin. Nesciunt tofu stumptown aliqua, retro synth master cleanse. Mustache cliche tempor, williamsburg carles vegan helvetica. Reprehenderit butcher retro keffiyeh dreamcatcher synth.</p>
                </b-tab>
            </b-tabs>
        </div>
    </div>
</template>
<script>
export default {
    name: 'SettingsCard'
}
</script>
<style>

</style>
