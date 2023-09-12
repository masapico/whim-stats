# Home

## 気まぐれスタッツとは

- 気になったデータを集めて可視化するサイト
- 気まぐれで対象をチョイスしているので、特にテーマはありません
- 肝心のデータ内容は気まぐれではないのでご安心ください

- スタッツ一覧は以下から閲覧できます
    - [スタッツ一覧へ](./stats.md)

## 利用しているデータについて

- 基本的にはオープンデータを利用しており、詳細は各データの出典に記載しています

## 可視化の工程について

- 統計の描画には Chart.js を利用
    - Pythonでデータ前処理を行いjson形式で保存
    - jsonデータをChart.jsに流し込み
    - データによっては補正が必要な場合もあり、詳細は各図ページに記載
    - サイトは mkdocs で作成し、Github Pages で公開しています

## 動作確認

- 以下のグラフが閲覧できない場合は何かおかしいので、別ブラウザなどで試してください

-----------------

<script src='./stats/chart.js'></script>

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
