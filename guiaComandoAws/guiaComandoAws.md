## configuração de usuario

🔹 Passos para criar um bucket S3 no VS Code

✅ 1. Instalação a extensão AWS Toolkit <br>

✅ 2. Configure suas credenciais da AWS No terminal do VS Code, configure suas credenciais usando o AWS CLI<br>

aws configure <br>

AWS Access Key ID [*****]: ***  <br>

AWS Secret Access Key [*****]: ***  <br>

Default region name [sa-east-1]: sa-east-1 <br>
Default output format [json]: json <br>

✅ 3. Abra o AWS Explorer no VS Code
Clique no AWS Explorer dentro do VS Code e conecte-se à sua conta AWS. <br>

✅ 4. Criar o bucket S3 <br>

aws s3api create-bucket --bucket meu-bucket --create-bucket-configuration LocationConstraint=sa-east-1 <br>

✅ 5. Testando upload de arquivos <br>

aws s3 cp "./dados.csv" s3://meu-bucket-vscode/ --region sa-east-1