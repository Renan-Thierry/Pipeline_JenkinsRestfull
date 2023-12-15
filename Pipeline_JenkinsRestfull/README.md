# Passo a Passo para Executar a Pipeline:

## 1. Preparação do Ambiente:
### Passo 1: Navegue até o diretório especificado
cd /var/run

### Passo 2: Conceda permissões ao arquivo docker.sock
sudo chmod 777 docker.sock

### Passo 3: Adicione um novo usuário chamado `jenkins`
useradd jenkins

### Passo 4: Adicione o usuário `jenkins` ao grupo `docker` para permitir a execução de comandos de superusuário.
sudo usermod -aG docker jenkins

### Passo 5: Verifique se o usuário `jenkins` foi adicionado ao grupo usando o comando:
grep docker /etc/group

## 2. Configuração da Pipeline no Jenkins:
# 1. Faça login no Jenkins.
# 2. Clique em: `+ Novo Tarefa`.
# 3. Insira o nome da pipeline.
# 4. Selecione `pipeline` nas opções disponíveis e clique em `Tudo certo`.
# 5. Adicione uma descrição a pipeline.
# 6. Desça até a seção `Pipeline`.
# 7. Em `definition`, clique em `Pipeline script` e selecione `Pipeline script from SCM`.
# 8. Na seção `SCM`, selecione a opção: `git`.
# 9. Insira a URL do repositório: `https://github.com/Renan-Thierry/Pipeline_JenkinsRestfull`.
# 10. Em `Branch Specifier`, insira o nome da branch que o repositório esta no github.
# 11. Clique em `Salvar` para concluir a configuração da pipeline.

## 3. Execução da Pipeline:
# - Depois de criar a pipeline, clique em `Construir agora`.
# - Em seguida, clique em `Open Blue Ocean` para gerenciar a pipeline
