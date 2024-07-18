<template>
    <div class="mx-auto max-w-7xl px-6 lg:px-8 py-8 lg:py-12">
        <LMap style="height: 350px" :zoom="6" :center="[47.21322, -1.559482]" :use-global-leaflet="false">
            <LTileLayer url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
                attribution="&amp;copy; <a href=&quot;https://www.openstreetmap.org/&quot;>OpenStreetMap</a> contributors"
                layer-type="base" name="OpenStreetMap" />
        </LMap>
    </div>
</template>