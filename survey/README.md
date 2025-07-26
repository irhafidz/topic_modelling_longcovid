<h3>📊 Interpretation Evaluation Results</h3>
<canvas id="interpretationChart" width="100%" height="400"></canvas>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
  const ctx = document.getElementById('interpretationChart').getContext('2d');
  new Chart(ctx, {
    type: 'bar',
    data: {
      labels: ['LDA', 'NMF', 'LSA', 'Top2Vec', 'BERTopic'],
      datasets: [
        {
          label: 'LLM Interpretability',
          backgroundColor: 'rgba(54, 162, 235, 0.6)',
          data: [4.77, 4.80, 4.03, 4.83, 4.77]
        },
        {
          label: 'LLM Relevance',
          backgroundColor: 'rgba(255, 206, 86, 0.6)',
          data: [3.93, 3.67, 3.47, 2.87, 4.13]
        },
        {
          label: 'Human Interpretability',
          backgroundColor: 'rgba(75, 192, 192, 0.6)',
          data: [4.11, 3.88, 3.60, 3.89, 3.65]
        },
        {
          label: 'Human Relevance',
          backgroundColor: 'rgba(255, 99, 132, 0.6)',
          data: [3.92, 3.84, 3.87, 3.20, 3.49]
        }
      ]
    },
    options: {
      responsive: true,
      plugins: {
        title: {
          display: true,
          text: 'Topic Interpretation Scores by Model (LLM vs Human)',
          font: {
            size: 18
          }
        },
        legend: {
          position: 'top'
        }
      },
      scales: {
        y: {
          beginAtZero: true,
          max: 5,
          title: {
            display: true,
            text: 'Score (1–5)'
          }
        },
        x: {
          title: {
            display: true,
            text: 'Model'
          }
        }
      }
    }
  });
</script>
