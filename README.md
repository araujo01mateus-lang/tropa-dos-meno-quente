# tropa-dos-meno-quente 
mport streamlit as st

st.title("Cadastro dos Meno Quentão")

nickname = st.text_input('Bota teu nick aí, mn')
nome = st.text_input('Bota teu nome de verdade aí')
server = st.text_input('Bota o server que tu joga')
whatsapp = st.text_input('Bota teu zap aí')
entrar = st.button('Enviar')

if entrar:
    with open("os_meno_quentao.txt", "a") as arquivo:
        arquivo.write(f"nickname: {nickname} | nome: {nome} | server: {server} | whatsapp: {whatsapp}\n")
    
    st.success('BRV! Se tu vai ser aprovado!')

    st.info("Para acessar o repositório, copie o comando abaixo no terminal:")
    st.code("git clone ssh://codeserver.dev.1036707a-14e8-4467-bfb6-ebe1d69cf0c0@codeserver.dev.1036707a-14e8-4467-bfb6-ebe1d69cf0c0.drush.in:2222/~/repository.git -b master tropa-dos-meno-quente")
