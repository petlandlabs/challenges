# Desafio Mobile

O objetivo do exercício é verificar sua familiaridade com react native, hooks, lógica e organização do código

Boa sorte e obrigado por participar!

## Sobre o desafio

Você deverá criar um aplicativo chamado "Agenda Petland", para que o cliente consiga fazer o agendamento do banho e tosa do seu pet. Criamos um mockup que deve ser seguido integralmente (https://www.figma.com/file/ixu0sBt4PVArMxJHSc4zxY/CHALLENGE-MOBILE?node-id=0%3A1).

## Sobre o aplicativo
O aplicativo possui 4 telas: listagem de pets, listagem de serviços de acordo com o pet selecionado, listagem de horários disponíveis de acordo com a data escolhida e finalizar agendamento.

- **Listagem de Pet**: seguir mockup do figma <br>
GET - https://api-homolog.geracaopet.com.br/api/challenges/mobile/pets/list <br>
Retorna um array de pets, com petId, petName e firstLetter. 
Ações esperadas: selecionar um pet, clicar em continuar e avançar para o próximo passo de selecionar o serviço de acordo com o pet escolhido.


- **Listagem de serviços**: seguir mockup figma <br>
GET - https://api-homolog.geracaopet.com.br/api/challenges/mobile/services?petId={petId} <br>
Retorna um objeto com 2 arrays: mainServices e additionalServices.
Ações esperadas: o usuário pode escolher apenas 1 main service e quantos additional services quiser. Depois de selecionado o serviço, clica em avançar e vai para o próximo passo.


- **Listagem de horários disponíveis**: seguir mockup figma <br>
GET - https://api-homolog.geracaopet.com.br/api/challenges/mobile/calendar?date={dia-selecionado}&servicesId={serviceId} <br>
Retorna um array de horários disponíveis de acordo com a data preenchida no input
Ações esperadas: quando um usuário selecionar uma data no calendário, chama o serviço passando a data selecionada no formato (aaaa-mm-dd), e uma lista de serviços selecionados no passo anterior, todos separados por virgula ex(123123,123123,124234). 
 
- **Criar agendamento**: seguir mockup figma <br>
POST - https://api-homolog.geracaopet.com.br/api/challenges/mobile/pre-appointment <br>
Ações esperadas: quando cliar no botão finalizar agendamento, enviar um post e no body colocar petId, servicesId, date (String) e startsAt (string). Date e startsAt é o que foi selecionado no calendário e horários disponíveis

```
{
    "petId": string, ex: "1"
    "servicesId": array com id do serviços, ex: ["60eda3d79478cf20bcb24533", "60ee5e7733c667497c093b6d"],
    "date" : "2022-02-03",
    "startsAt" : "09:00"
}
```

## Entrega do Projeto
- Vamos focar em avaliar o que foi proposto para o exercício, mas se não conseguir conter sua criatividade e quiser incrementar a aplicação, fique à vontade. Só não deixe de entregar o essencial. ;)
- Ao finalizar, suba a sua proposta para o projeto que você criou no GitHub
- Envie-nos o link do projeto.


 ##### Pronto! Basta aguardar que vamos entrar em contato
