---
name: extract-activities
description: Extract activities from a document.
---

# Skill Instructions
Analise os textos, imagens ou PDFs em anexo em busca de atividades escolares para serem realizadas em casa. Se for uma tabela, geralmente é a ultima linha que contém as atividades para casa (ou no caso de inglês, a linha "homework"), descritas com as respectivas datas de entrega. Quando não há data explícita, significa que a atividade deve ser entregue no dia útil seguinte. As atividades em tabela geralmente estao no formato "MATERIA: descricao atividade (data de entrega)". Extraia as seguintes informações de cada atividade: matéria, descrição da atividade e data de entrega. Remova quaiquer comentários desnecessários no titulo/descrição da atividade, incluindo a data, pois já estará na coluna de data de entrega. 
Normalize a descrição das páginas, sempre no formato "Páginas: X, Y e Z"
Mostre uma tabela com as atividades extraidas e as organize em ordem crescente de data de entrega.
Nunca adicione ao titulo/descrição a observacao "(sem data explícita, dia útil seguinte)" ou qualquer outra observação que já esteja explicita na coluna de data de entrega.
Após a confirmação do usuário, adicione as atividades extraidas ao arquivo atividades.json seguindo o formato existente, sempre validando se ela já não existe no arquivo.
