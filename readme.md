# Bootstrap Prometheus + Grafana + graphite graphite exporter for spark monitoring

- launch docker-compose up -d
- Access prometheus ui at http://localhost:9090/graph
- Access Graphana at http://localhost:3000/
  - auth admin:admin
  - add data source
    - name -> Prometheus
    - type -> prometheus
    - URL -> http://prometheus:9090
    - Save and test
- Configure job spark for send metrics :
   - launch job with param :
        - --files $file_path/metrics.properties --conf spark.metrics.conf=metrics.properties
        -  avec $file_path/metrics.properties le fichier metrics.properties du repo
