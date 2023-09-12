# Home

- 気になったデータを集めて可視化するサイト
- 完全な気まぐれなので特にこだわりはありません

## 利用しているデータについて

- 基本的にはオープンデータを利用しており、詳細は各データの出典に記載しています

<script src='js/chart.js'></script>

<div>
  <canvas id="myChart"></canvas>
</div>

<script>
  const ctx = document.getElementById('myChart');

  new Chart(ctx, {
    type: 'bar',
    data: {
      labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
      datasets: [{
        label: '# of Votes',
        data: [12, 19, 3, 5, 2, 3],
        borderWidth: 1
      }]
    },
    options: {
      scales: {
        y: {
          beginAtZero: true
        }
      }
    }
  });
</script>
