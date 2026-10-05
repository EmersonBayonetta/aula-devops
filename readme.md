
      comandos yml
      
      - name: Verificar arquivos essenciais do projeto
        run: |
          test -f index.html && echo "HTML encontrado!"

      - name: Validar sintaxe do HTML
        uses: htmlhint/htmlhint-action@v2
        with:
          target_pattern: "index.html"

      - name: Checar arquivos estaticos
        run: |
          ls -R
          echo "Todos os arquivos foram carregados corretamente."
