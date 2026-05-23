Internet
   |
   v
+-------------------+
| Public EC2        |
| API + III Engine  |
| Port 3111         |
+-------------------+
          |
          | private subnet
          v
+-------------------+
| Caller Worker     |
+-------------------+
          |
          v
+-------------------+
| Math Worker       |
+-------------------+

curl -X POST http://<public-ip>:3111/math/add-two-numbers \
-H "Content-Type: application/json" \
-d '{"a":10,"b":20}'
Response
{
  "result": 30
}

terraform init
terraform apply

ssh ubuntu@<public-ip>

git clone <repo>
docker compose up -d --build
