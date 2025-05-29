# Rede Social para Pets (Cachorros e Gatos)

- Donos podem cadastrar seus animais de estimação.
- Animais são vinculados a um dono.
- Donos podem adicionar outros amigos humanos ou não.
- Donos podem postar notícias e curtir outros animais.
- Donos podem criar uma agenda e participar de eventos sociais.

## Modelo de Dados

### 1. Usuário (Dono)
- **ID** (chave primária)
- **Nome** (string)
- **Email** (string)
- **Senha** (string)
- **Lista de Amigos** (array de IDs de outros usuários)

### 2. Animal de Estimação
- **ID** (chave primária)
- **Nome** (string)
- **Tipo** (enum: cachorro/gato)
- **Idade** (inteiro)
- **Dono_ID** (chave estrangeira referenciando Usuário)

### 3. Postagem
- **ID** (chave primária)
- **Dono_ID** (chave estrangeira referenciando Usuário)
- **Conteúdo** (texto, foto, vídeo)
- **Data de Publicação** (data/hora)
- **Lista de Curtidas** (array de IDs de usuários que curtiram)

### 4. Amizade
- **ID** (chave primária)
- **Usuário1_ID** (chave estrangeira referenciando Usuário)
- **Usuário2_ID** (chave estrangeira referenciando Usuário)

### 5. Evento
- **ID** (chave primária)
- **Nome** (string)
- **Data** (data/hora)
- **Localização** (string)
- **Lista de Participantes** (array de IDs de usuários)
