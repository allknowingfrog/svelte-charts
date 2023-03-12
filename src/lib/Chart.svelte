<script>
  import { onMount } from 'svelte'
  import Chart from 'chart.js/auto'
  import 'chartjs-adapter-luxon'

  let timeCanvas

  const timeData = [
    {
      x: "2023-01-01T00:00:00",
      y: 11
    },
    {
      x: "2023-01-01T12:00:00",
      y: 12
    },
    {
      x: "2023-01-03T00:00:00",
      y: 14
    },
    {
      x: "2023-01-04T00:00:00",
      y: 15
    },
    {
      x: "2023-01-05T00:00:00",
      y: 14
    },
    {
      x: "2023-01-08T00:00:00",
      y: 10
    }
  ]

  onMount(() => {
    new Chart(
      timeCanvas,
      {
        type: 'line',
        options: {
          scales: {
            x: {
              type: 'time',
              time: {
                unit: 'day'
              }
            },
            y: {
              suggestedMin: 0,
              suggestedMax: 20
            }
          }
        },
        data: {
          datasets: [
            {
              label: 'Time Data',
              data: timeData
            }
          ]
        }
      }
    )
  })
</script>

<canvas bind:this={timeCanvas}></canvas>

<style>
  canvas {
    width: 800px;
  }
</style>
