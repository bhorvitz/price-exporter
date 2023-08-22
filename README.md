# price-exporter
Run price-exporter as a service

Add to your prometheus.yml under scrape configs:
  - job_name: "xch-price"
    static_configs:
    - targets: ['localhost:9444']
      labels:
        application: 'chia-market'

Metric chia_price_usd should then be available in Grafana
