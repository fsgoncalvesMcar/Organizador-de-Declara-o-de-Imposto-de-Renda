# Organizador-de-Declara-o-de-Imposto-de-Renda

Modelo de Planilha
1. Resumo_Geral
| Campo                | Valor                    |
|----------------------|--------------------------|
| Nome completo        |                          |
| CPF                  |                          |
| Ano-base             |                          |
| Tipo de declaração   | Completa / Simplificada  |
| Imposto a pagar      |                          |
| Imposto a restituir  |                          |

2. Rendimentos_Tributáveis
| Fonte Pagadora | CNPJ        | Valor Bruto | IR Retido |
|----------------|-------------|-------------|-----------|
|                |             |             |           |

3. Rendimentos_Isentos
| Fonte      | Valor     | Descrição                |
|------------|-----------|--------------------------|
|            |           |                          |

4. Bens_e_Direitos
| Tipo        | Localização | Situação 31/12/2024 | Situação 31/12/2023 |
|-------------|-------------|---------------------|---------------------|
|             |             |                     |                     |

5. Dívidas_e_Ônus
| Instituição | Tipo de Dívida | Valor 31/12/2024 |
|-------------|----------------|------------------|
|             |                |                  |

6. Pagamentos_Efetuados
| Favorecido   | CPF/CNPJ   | Tipo de Despesa | Valor Pago |
|--------------|------------|-----------------|------------|
|              |            |                 |            |

7. Dependentes
| Nome     | CPF       | Grau de Parentesco | Data de Nascimento |
|----------|-----------|--------------------|---------------------|
|          |           |                    |                     |

Recursos que posso adicionar:
1. Fórmulas de Soma Automática: Nas abas de rendimentos e pagamentos, podemos usar =SOMASE(...) ou =SOMA(...) para totalizar valores automaticamente.

2. Destaques com Formatação Condicional: Por exemplo, podemos destacar:
Valores acima de determinado limite
Células em branco que precisam ser preenchidas
Pagamentos de saúde ou educação

3. Validação de CPF: Adicionar uma fórmula que verifica se o CPF tem 11 dígitos numéricos:
=E(ÉTEXTO(A2);NÚM.CARACT(A2)=11)
(Supondo que o CPF esteja na célula A2.)

4. Cálculo Automático do Saldo do IR: Na aba de Resumo, podemos calcular:
=SE([@‘IR Retido’] > [@‘IR Devido’]; “Restituição”; “Imposto a Pagar”)

5. Botão para Exportar PDF (via VBA): Com um pequeno código, adicionamos um botão que exporta a aba “Resumo_Geral” para um PDF.

6. Proteção e Bloqueio de Células: Evitar que fórmulas sejam apagadas por acidentes
