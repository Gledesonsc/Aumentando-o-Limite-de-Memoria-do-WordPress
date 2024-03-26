# Aumentando o Limite de Memória do WordPress

🚀 **Introdução:**

Nesta documentação, vamos aprender como aumentar o limite de memória do WordPress no servidor usando o arquivo `php.ini`.

✅ **Pré-requisitos:**

- Acesso SSH à sua VPS.
- Conhecimento básico do terminal Linux.
- WordPress instalado na sua VPS.

🔧 **Passos:**

1. **Acesso SSH à VPS:**

   Acesse sua VPS usando SSH. Você pode usar um cliente SSH como o PuTTY (Windows) ou Terminal (Mac/Linux).

   ```bash
   ssh seu_usuario@seu_ip_da_vps
   ```

2. **Encontre o Arquivo `php.ini`:**

   Use o comando `php -i | grep "php.ini"` para encontrar o local do arquivo `php.ini`.

   ```bash
   php -i | grep "php.ini"
   ```

3. **Edite o `php.ini`:**

   Use um editor de texto como o `nano` para editar o arquivo `php.ini`.

   ```bash
   nano /caminho/para/o/seu/php.ini
   ```

4. **Localize a Diretiva `upload_max_filesize`:**

   Use `Ctrl + W` no `nano` para pesquisar por `upload_max_filesize`.

5. **Aumente o Limite de Memória:**

   Altere o valor da diretiva `upload_max_filesize` para o tamanho desejado, por exemplo, `64M` para permitir uploads de até 64 MB.

   ```ini
   upload_max_filesize = 64M
   ```

6. **Salve as Alterações:**

   Pressione `Ctrl + O` para salvar as alterações, `Enter` para confirmar o nome do arquivo e `Ctrl + X` para sair do `nano`.

7. **Reinicie o LiteSpeed:**

   Reinicie o LiteSpeed para aplicar as alterações feitas no `php.ini`.

   ```bash
   systemctl restart lsws
   ```

🎉 **Conclusão:**

Agora você aumentou com sucesso o limite de memória do WordPress no servidor, permitindo uploads de arquivos maiores.
