# 📊 Projeto de Previsão Salarial com ASP.NET Core e ML.NET

## 👥 Integrantes do Grupo

-   João Vitor Valaitis Paulo - RM: 553972
-   Carlos Eduardo Ariza - RM: 553461
-   Fernando Shinji Tanigushi - RM: 553587
---

## 📌 Descrição do Projeto

Este projeto foi desenvolvido como parte de uma atividade prática utilizando **ASP.NET Core** e **ML.NET** para realizar **previsões de salário** com base em duas variáveis: **idade** e **anos de experiência**.

Foi implementado um modelo de **regressão** com o algoritmo **FastTree**, utilizando uma divisão de dados de **70% para treino** e **30% para teste**. Os dados estão em formato CSV na pasta `Data`.

A aplicação disponibiliza uma API REST documentada com **Swagger**, permitindo enviar dados de entrada e obter uma predição como resposta.

---

## 🗃️ Estrutura do Projeto

├── Controllers/

│ └── PredictController.cs
├── Models/
│ ├── EntradaModel.cs
│ └── PrevisaoModel.cs

├── Services/
│ └── MLService.cs

├── Data/
│ └── dados.csv

├── appsettings.json

├── Program.cs

├── Startup.cs

├── PrevisaoML.sln


🧠 Treinamento do Modelo


O modelo utiliza o algoritmo de regressão FastTree.

Ao iniciar a aplicação, o modelo é automaticamente treinado com os dados presentes no CSV.

A divisão dos dados é de 70% para treino e 30% para teste.

A métrica de desempenho R² é exibida no console após o treino:

R²: 0.98

🚀 Executando a API

Baixe o projeto(esta zipado neste github:https://github.com/AganeSenpai/CP5e6

Abra a solução PrevisaoML.sln no Visual Studio.

Execute o projeto (F5 ou dotnet run).

Acesse o Swagger:

https://localhost:<porta>/swagger
🔮 Exemplo de Execução (Swagger)
Endpoint:

POST /api/predict
Requisição de Exemplo:

{
  "idade": 30,
  "experiencia": 5
}


Resposta Esperada:

{
  "predicao": 3485.23
}
