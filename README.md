class FilaFIFO:
  def __init__(self):
    self.fila = []




  def adicionar(self,item):
      self.fila.append(item)
      print(f"Adicionado: {item}")

  def remover(self):
      if self.esta_vazia():
        return "A fila está vazia!"
      return self.fila.pop(0)

  def esta_vazia(self):
      return len(self.fila) == 0

  def tamanho(self):
      return len(self.fila)

  def frente(self):
      if self.esta_vazia():
        return "A fila está vazia!"
      return self.fila[0]

  def exibir(self):
      if self.esta_vazia():
        print("A fila está vazia!")
      else:
        print("Fila:", "->".join(self.fila))


# Exemplo de uso
fila = FilaFIFO()
fila.adicionar("Processo 1")
fila.adicionar("Processo 2")
fila.exibir() # Exibe a fila atual
print(f"Item da frente: {fila.frente()}")
print(f"Removido: {fila.remover()}")
fila.exibir() # Exibe a fila após a remoção
print(f"Tamanho da fila: {fila.tamanho()}")