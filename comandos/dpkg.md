O `dpkg` é um utilitário de linha de comando utilizado em sistemas Linux baseados em Debian (como o Ubuntu) para gerenciar pacotes DEB. Aqui estão alguns dos principais comandos e opções do `dpkg`:

1. **Instalar um pacote DEB:**
   ```
   dpkg -i nome-do-pacote.deb
   ```

2. **Remover um pacote DEB (mantendo arquivos de configuração):**
   ```
   dpkg -r nome-do-pacote
   ```

3. **Remover um pacote DEB (removendo arquivos de configuração):**
   ```
   dpkg -P nome-do-pacote
   ```

4. **Listar pacotes instalados:**
   ```
   dpkg -l
   ```

5. **Exibir informações detalhadas sobre um pacote instalado:**
   ```
   dpkg -p nome-do-pacote
   ```

6. **Listar arquivos de um pacote instalado:**
   ```
   dpkg -L nome-do-pacote
   ```

7. **Procurar por um pacote específico:**
   ```
   dpkg -l | grep nome-do-pacote
   ```

8. **Reconfigurar um pacote:**
   ```
   dpkg-reconfigure nome-do-pacote
   ```

9. **Verificar a integridade dos pacotes instalados:**
   ```
   dpkg --audit
   ```

10. **Listar pacotes quebrados:**
    ```
    dpkg --get-selections | awk '$2 ~ /install/ {print $1}' | xargs dpkg -l
    ```

11. **Baixar um pacote DEB sem instalá-lo:**
    ```
    apt-get download nome-do-pacote
    ```

Lembre-se de que o `dpkg` lida diretamente com os pacotes DEB, mas não resolve automaticamente dependências. Portanto, é comum usar ferramentas de gerenciamento de pacotes de nível mais alto, como o `apt` ou o `apt-get`, que cuidam das dependências automaticamente e simplificam o gerenciamento de pacotes no Debian e em distribuições derivadas.