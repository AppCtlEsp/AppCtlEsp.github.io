# Cadastro — Controle Esportes

Formulário de autocadastro de jogadores do app **Controle Esportes**.
A pessoa recebe um link com o código do convite e preenche a própria ficha,
gravando direto no banco do grupo.

Endereço: `.../?t=<código do convite>` — sem o código, a página não mostra nada.

## Por que este repositório é público

O GitHub Pages só publica páginas a partir de repositórios públicos em contas
gratuitas. Isso não expõe nada: a página contém apenas o endereço do projeto
Supabase e a chave `anon`, que é **feita para ficar no cliente** e já vai
embutida no aplicativo.

Quem protege os dados é o banco:
- as regras de RLS impedem qualquer leitura de dados do grupo por esta página;
- gravar um jogador só é possível com um **token de convite válido e não
  expirado**, verificado no servidor;
- fotos só podem ser enviadas para a pasta de autocadastro do grupo daquele
  convite, com no máximo 5 MB, e nunca sobrescrevem fotos existentes.

O código do app fica em repositório separado e privado.
