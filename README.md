# Gerador de Guias

App desktop que gera, em segundos, as guias de atendimento que a clínica entrega aos planos de saúde todo mês. Antes isso era preenchido à mão, paciente por paciente.

> Código privado porque usa a agenda real dos pacientes. Aqui ficam o projeto e o que aprendi.

## O problema
Cada plano tem seu próprio modelo de guia, e cada paciente tem uma agenda semanal diferente. Preencher datas e sessões à mão, todo mês, tomava tempo e gerava erro.

## O que o app faz
- Lê a agenda semanal de cada paciente e transforma em datas reais do mês
- Preenche o modelo Excel certo de cada plano (4 planos, cada um com seu template)
- Salva tudo organizado: `Guias/<mês>/<plano>/<paciente>.xlsx`
- Tela de cronogramas para cadastrar e editar pacientes e sessões, com backup automático antes de cada edição
- Versão standalone (.exe) que roda em qualquer PC da clínica, até de pendrive

## Stack
Python · Tkinter · openpyxl · PyInstaller

## Como evoluiu
Já está na versão 4. Cada versão nasceu de uma dor real: mais planos, edição de cronograma dentro do app, backup automático, executável standalone. Também documentei a arquitetura e marquei o código legado, pra saber o que pode ser apagado.

## O que aprendi
- Manipular planilhas Excel por código mantendo a formatação dos modelos
- Lidar com datas (dia da semana → datas do mês)
- Criar interface desktop simples para quem não é da área de TI
- Documentar e limpar um projeto que cresceu rápido
