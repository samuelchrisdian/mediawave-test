<template>
    <div class="mx-auto max-w-7xl px-6 lg:px-8 py-8 lg:py-12">
        <highchart :options="chartOptions" :modules="['sankey', 'dependency-wheel']"></highchart>
    </div>
</template>
<script>
export default {
    name: "index",
    data() {
        return {
            chartOptions: {
                chart: {
                    type: 'bar',
                    height: 1500
                },
                title: {
                    text: 'Social Media User by Province',
                    align: 'left'
                },
                subtitle: {
                    text: 'Dummy Data',
                    align: 'left'
                },
                xAxis: {
                    categories: [
                        "Aceh",
                        "Sumatera Utara",
                        "Sumatera Barat",
                        "Riau",
                        "Jambi",
                        "Sumatera Selatan",
                        "Bengkulu",
                        "Lampung",
                        "Kepulauan Bangka Belitung",
                        "Kepulauan Riau",
                        "DKI Jakarta",
                        "Jawa Barat",
                        "Jawa Tengah",
                        "DI Yogyakarta",
                        "Jawa Timur",
                        "Banten",
                        "Bali",
                        "Nusa Tenggara Barat",
                        "Nusa Tenggara Timur",
                        "Kalimantan Barat",
                        "Kalimantan Tengah",
                        "Kalimantan Selatan",
                        "Kalimantan Timur",
                        "Kalimantan Utara",
                        "Sulawesi Utara",
                        "Sulawesi Tengah",
                        "Sulawesi Selatan",
                        "Sulawesi Tenggara",
                        "Gorontalo",
                        "Sulawesi Barat",
                        "Maluku",
                        "Maluku Utara",
                        "Papua Barat",
                        "Papua",
                        "Papua Tengah",
                        "Papua Pegunungan",
                        "Papua Selatan",
                        "Papua Barat Daya"
                    ],
                    title: {
                        text: null
                    },
                    gridLineWidth: 1,
                    lineWidth: 0
                },
                yAxis: {
                    min: 0,
                    title: {
                        text: 'User (millions)',
                        align: 'high'
                    },
                    labels: {
                        overflow: 'justify'
                    },
                    gridLineWidth: 0
                },
                tooltip: {
                    valueSuffix: ' millions'
                },
                plotOptions: {
                    bar: {
                        borderRadius: '50%',
                        dataLabels: {
                            enabled: true
                        },
                        groupPadding: 0.1
                    }
                },
                legend: {
                    layout: 'vertical',
                    align: 'right',
                    verticalAlign: 'top',
                    x: -40,
                    y: 80,
                    floating: true,
                    borderWidth: 1,
                    backgroundColor: '#FFFFFF',
                    shadow: true
                },
                credits: {
                    enabled: false
                },
                series: [
                    {
                        name: 'Instagram',
                        data: [10.5, 12.3, 9.8, 11.7, 8.2, 9.5, 7.4, 8.8, 7.1, 6.9, 15.2, 14.3, 13.4, 10.9, 14.7, 11.5, 9.6, 7.3, 6.8, 5.7, 5.2, 4.9, 6.3, 4.5, 3.8, 5.1, 8.7, 6.4, 3.6, 4.8, 3.4, 2.9, 3.2, 4.1, 2.6, 2.3, 2.5, 2.2]
                    },
                    {
                        name: 'Facebook',
                        data: [15.3, 14.1, 10.2, 12.5, 9.7, 10.9, 8.5, 9.2, 7.8, 7.6, 16.4, 15.1, 14.6, 12.2, 15.3, 12.4, 10.3, 8.1, 7.4, 6.3, 6.1, 5.7, 7.5, 5.0, 4.3, 5.7, 9.3, 7.2, 4.0, 5.4, 3.8, 3.3, 3.5, 4.5, 2.9, 2.7, 2.8, 2.4]
                    },
                    {
                        name: 'Twitter',
                        data: [8.2, 7.5, 5.9, 7.1, 5.3, 6.2, 4.7, 5.5, 4.1, 4.0, 9.5, 8.9, 8.3, 6.7, 9.2, 7.4, 6.1, 4.8, 4.3, 3.7, 3.5, 3.3, 4.2, 2.8, 2.4, 3.2, 5.3, 4.1, 2.3, 3.0, 2.1, 1.9, 2.0, 2.6, 1.7, 1.5, 1.6, 1.4]
                    },
                    {
                        name: 'TikTok',
                        data: [12.7, 11.9, 9.3, 10.8, 8.4, 9.6, 7.2, 8.3, 6.5, 6.3, 13.8, 12.6, 11.5, 9.1, 13.2, 10.2, 8.8, 7.1, 6.6, 5.4, 5.1, 4.7, 6.2, 4.2, 3.6, 4.5, 7.4, 5.9, 3.5, 4.4, 3.1, 2.7, 3.0, 3.8, 2.3, 2.0, 2.2, 1.9]
                    }
                ]
            },
        };
    },
};
</script>