# janela.py
import tkinter as tk
from tkinter import messagebox  


def clique_do_botao():
    nome_digitado = campo_texto.get()

    if nome_digitado:
        messagebox.showinfo("Mensagem", f"Olá, {nome_digitado}! Você clicou com sucesso!")
    else:
        messagebox.showwarning("Aviso", "Por favor, digite seu nome primeiro!")


# Criação da janela principal
janela = tk.Tk()
janela.title("Minha Tela em Python")
janela.geometry("300x230") 

#  Criação do texto (Label)
texto = tk.Label(janela, text="Digite seu nome abaixo:", font=("Arial", 11))
texto.pack(pady=(20, 5))

#  Novo elemento: Campo de entrada de texto (Entry)
campo_texto = tk.Entry(janela, font=("Arial", 11), width=25)
campo_texto.pack(pady=5)

# Criação do botão
botao = tk.Button(
    janela,
    text="Clique aqui",
    font=("Arial", 12),
    bg="#4CAF50",
    fg="white",
    command=clique_do_botao,
)
botao.pack(pady=15)

# Mantém a janela aberta
janela.mainloop()
