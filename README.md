# Criando-um-Personal-Trainer-IA-com-Boas-Pr-ticas-de-Prompt-Engineer
import nltk
from nltk.tokenize import word_tokenize
from nltk.corpus import stopwords

# Carregar o corpus de stopwords
stop_words = set(stopwords.words('portuguese'))

# Definir a função de processamento de linguagem natural
def processar_linguagem(texto):
    # Tokenizar o texto
    tokens = word_tokenize(texto)
    
    # Remover stopwords
    tokens = [token for token in tokens if token not in stop_words]
    
    # Retornar a lista de tokens
    return tokens

# Definir a função de geração de linguagem
def gerar_linguagem(tokens):
    # Gerar uma frase a partir dos tokens
    frase = ' '.join(tokens)
    
    # Retornar a frase
    return frase

# Testar o modelo
texto = "Eu quero treinar meu peito hoje."
tokens = processar_linguagem(texto)
frase = gerar_linguagem(tokens)
print(frase)
