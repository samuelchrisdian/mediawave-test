<template>
    <div class="mx-auto max-w-7xl px-6 lg:px-8 py-8 lg:py-12">
        <LMap style="height: 480px" :zoom="5" :center="[-0.622793, 116.631158]" :use-global-leaflet="false">
            <LTileLayer url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
                attribution="&amp;copy; <a href=&quot;https://www.openstreetmap.org/&quot;>OpenStreetMap</a> contributors"
                layer-type="base" name="OpenStreetMap" />
            <LCircleMarker v-for="(province, index) in provinces" :key="index" :lat-lng="province.latLng"
                :radius="province.radius" :color="province.color" />
        </LMap>
    </div>
</template>

<script>
export default {
    name: "MapExample",
    data() {
        return {
            provinces: [
                { name: "Aceh", latLng: [4.695135, 96.749397], radius: 15, color: 'red' },
                { name: "Sumatera Utara", latLng: [3.585242, 98.675598], radius: 18, color: 'blue' },
                { name: "Sumatera Barat", latLng: [-0.941027, 100.354271], radius: 12, color: 'green' },
                { name: "Riau", latLng: [0.507068, 101.447777], radius: 14, color: 'orange' },
                { name: "Jambi", latLng: [-1.485834, 102.438057], radius: 10, color: 'purple' },
                { name: "Sumatera Selatan", latLng: [-3.319437, 104.914551], radius: 16, color: 'cyan' },
                { name: "Bengkulu", latLng: [-3.800443, 102.265541], radius: 11, color: 'magenta' },
                { name: "Lampung", latLng: [-4.558584, 105.406807], radius: 13, color: 'yellow' },
                { name: "Kepulauan Bangka Belitung", latLng: [-2.741051, 106.440586], radius: 9, color: 'pink' },
                { name: "Kepulauan Riau", latLng: [3.945641, 108.142866], radius: 12, color: 'brown' },
                { name: "DKI Jakarta", latLng: [-6.208763, 106.845599], radius: 20, color: 'darkblue' },
                { name: "Jawa Barat", latLng: [-6.914864, 107.609810], radius: 19, color: 'darkgreen' },
                { name: "Jawa Tengah", latLng: [-7.566618, 110.831787], radius: 17, color: 'darkred' },
                { name: "DI Yogyakarta", latLng: [-7.795580, 110.369492], radius: 10, color: 'navy' },
                { name: "Jawa Timur", latLng: [-7.250445, 112.768845], radius: 18, color: 'lime' },
                { name: "Banten", latLng: [-6.120000, 106.150276], radius: 16, color: 'teal' },
                { name: "Bali", latLng: [-8.340539, 115.092107], radius: 14, color: 'aqua' },
                { name: "Nusa Tenggara Barat", latLng: [-8.652933, 117.361647], radius: 12, color: 'olive' },
                { name: "Nusa Tenggara Timur", latLng: [-9.152495, 123.600029], radius: 10, color: 'salmon' },
                { name: "Kalimantan Barat", latLng: [0.132399, 111.096985], radius: 13, color: 'khaki' },
                { name: "Kalimantan Tengah", latLng: [-1.681487, 113.382355], radius: 12, color: 'gold' },
                { name: "Kalimantan Selatan", latLng: [-3.092641, 115.283758], radius: 14, color: 'silver' },
                { name: "Kalimantan Timur", latLng: [0.538653, 116.419389], radius: 16, color: 'coral' },
                { name: "Kalimantan Utara", latLng: [3.471227, 117.596607], radius: 11, color: 'turquoise' },
                { name: "Sulawesi Utara", latLng: [1.493056, 124.841250], radius: 13, color: 'lavender' },
                { name: "Sulawesi Tengah", latLng: [-1.430691, 121.445617], radius: 15, color: 'plum' },
                { name: "Sulawesi Selatan", latLng: [-3.668799, 119.974054], radius: 18, color: 'crimson' },
                { name: "Sulawesi Tenggara", latLng: [-4.129660, 122.174918], radius: 12, color: 'chartreuse' },
                { name: "Gorontalo", latLng: [0.699937, 122.446723], radius: 10, color: 'beige' },
                { name: "Sulawesi Barat", latLng: [-2.844946, 119.232078], radius: 9, color: 'bisque' },
                { name: "Maluku", latLng: [-3.238461, 130.145273], radius: 11, color: 'honeydew' },
                { name: "Maluku Utara", latLng: [0.634755, 127.970536], radius: 10, color: 'peru' },
                { name: "Papua Barat", latLng: [-1.336115, 133.174716], radius: 12, color: 'orchid' },
                { name: "Papua", latLng: [-4.269928, 138.080353], radius: 17, color: 'wheat' },
                { name: "Papua Tengah", latLng: [-3.756928, 136.752762], radius: 14, color: 'thistle' },
                { name: "Papua Pegunungan", latLng: [-4.083420, 138.200150], radius: 11, color: 'sienna' },
                { name: "Papua Selatan", latLng: [-6.232905, 140.650672], radius: 9, color: 'rosybrown' },
                { name: "Papua Barat Daya", latLng: [-1.252846, 132.556712], radius: 8, color: 'slateblue' }
            ]
        };
    }
};
</script>