





Exercício de revisão:
    É necesário modelar um esquema de banco de dados para um fluxo ou funcionalidade dentro de um sistema de submissão de projetos em uma instituição.
    Em uma instituição, há professores/pesquisadores que submetem projetos de extensão. Um projeto possui título, resumo, coordenador (professor/pesquisador),
    equipe (relação de professores/pesquisadores), área de pesquisa (técnologia, saúde, humanas, social), uma instituição responsável. Uma instituição tem
    nome, sigla e endereço. Um professor/pesquisador possui nome, email, cpf, número de celular. Todo o projeto submetido precisa passar por uma avaliação.
    A avaliação é composta por uma submissão de projeto, um avaliador responsável (professor/pesquisador), um avaliador suplente (professor/pesquisador),
    um campo para parecer, data limite de parecer, resultado (aprovado, reprovado, em correção)

    1º passo: identificar entidades
    2º passo: identificar atributos
    3º passo: identificar relacionamentos
    4º passo: identificar cardinalidades


    Entidades:
        - Professor (ligado com Projeto, Avaliacao)
            - Nome
            - Email
            - CPF (id)
            - Celular
        - Projeto (ligado com Avaliacao, Professor, Area, Instituicao)
            - Título
            - Resumo
            - Equipe (Rótulo com Professor) 1...n / 1...n
            - Coordenador (Rótulo com Professor) 1...n / 1...n
            - idProjeto
        - Avaliacao (núcleo do nosso banco de dados) (ligado com Professor, Projeto, Resultado)
            - idAvaliacao
            - Responsavel (Rótulo com Professor)
            - Suplente (Rótulo com Professor)
            - Parecer
            - data
        - Instituicao (ligado com Projeto)
            - Nome
            - Sigla
            - Endereco
            - idInstituicao
        - Area (ligado com Projeto)
            - Descricao
            - idArea
        - Resultado (ligado com Avaliacao)
            - idResultado
            - Descricao
        



Relacionamento indica que UM ou MAIS ATRIBUTOS de uma entidade VISITA outra
O lado que está com o N da cardinalidade, ele puxa a chave estrangeira. 
Deve ser atributo identificador na entidade de origem
