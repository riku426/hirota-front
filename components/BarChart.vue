<script>
import { Bar } from 'vue-chartjs'
export default {
  extends: Bar,
  data(){
    return {
        chartdata: {
            labels: ['月', '火','水','木', '金', '土', '日'],
            datasets: [
                {
                label: ['１週間の飲酒量'],
                backgroundColor: '#f87979',
                data: [1, 3, 1, 2, 0, 3, 1]
                }
            ]
        },
        options: {
            responsive: true,
            maintainAspectRatio: false
        }
    }
  },
  mounted () {
    this.renderChart(this.chartdata, this.options)
  }
}
</script>