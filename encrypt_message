import tkinter as tk
from tkinter import messagebox
from cryptography.fernet import Fernet


# Function to generate a key
def generate_key():
    key = Fernet.generate_key()
    return key


# Function to encrypt a message
def encrypt_message(key, message):
    f = Fernet(key)
    encrypted_message = f.encrypt(message.encode())
    return encrypted_message


# Function to decrypt a message
def decrypt_message(key, encrypted_message):
    f = Fernet(key)
    decrypted_message = f.decrypt(encrypted_message).decode()
    return decrypted_message


# Callback function for encrypting a message
def encrypt():
    key = key_entry.get().encode()
    message = message_entry.get()

    if key and message:
        try:
            encrypted_message = encrypt_message(key, message)
            result_entry.delete(0, tk.END)
            result_entry.insert(0, encrypted_message.decode())
        except Exception as e:
            messagebox.showerror("Error", f"Encryption failed: {e}")
    else:
        messagebox.showwarning("Warning", "Please provide both a key and a message.")


# Callback function for decrypting a message
def decrypt():
    key = key_entry.get().encode()
    encrypted_message = message_entry.get()

    if key and encrypted_message:
        try:
            decrypted_message = decrypt_message(key, encrypted_message.encode())
            result_entry.delete(0, tk.END)
            result_entry.insert(0, decrypted_message)
        except Exception as e:
            messagebox.showerror("Error", f"Decryption failed: {e}")
    else:
        messagebox.showwarning("Warning", "Please provide both a key and a message.")


# Callback function for generating a new key
def generate_new_key():
    key = generate_key()
    key_entry.delete(0, tk.END)
    key_entry.insert(0, key.decode())


# Create the main window
root = tk.Tk()
root.title("Encryption/Decryption Tool")

# Create and place the widgets
tk.Label(root, text="Key (Base64):").grid(row=0, column=0, padx=10, pady=10)
key_entry = tk.Entry(root, width=60)
key_entry.grid(row=0, column=1, padx=10, pady=10)

tk.Button(root, text="Generate Key", command=generate_new_key).grid(row=0, column=2, padx=10, pady=10)

tk.Label(root, text="Message:").grid(row=1, column=0, padx=10, pady=10)
message_entry = tk.Entry(root, width=60)
message_entry.grid(row=1, column=1, padx=10, pady=10)

tk.Button(root, text="Encrypt", command=encrypt).grid(row=2, column=0, padx=10, pady=10)
tk.Button(root, text="Decrypt", command=decrypt).grid(row=2, column=1, padx=10, pady=10)

tk.Label(root, text="Result:").grid(row=3, column=0, padx=10, pady=10)
result_entry = tk.Entry(root, width=60)
result_entry.grid(row=3, column=1, padx=10, pady=10)

# Start the main loop
root.mainloop()