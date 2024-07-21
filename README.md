# Tela de Login em React Native

Este é um aplicativo simples de tela de login utilizando React Native e Expo. A tela de login contém dois campos de texto (um para o usuário e outro para a senha) e um botão de login. Flexbox é utilizado para organizar os elementos de maneira responsiva e centralizada na tela.

## Visão Geral

Este projeto demonstra como criar uma interface de login básica em React Native, utilizando Flexbox para layout. O projeto é ideal para iniciantes que desejam aprender sobre layouts responsivos e como gerenciar estados em React Native.

## Funcionalidades

- Campo de texto para usuário.
- Campo de texto para senha (com ocultação de texto).
- Botão de login que exibe um alerta com os valores inseridos.

## Tecnologias Utilizadas

- React Native
- Expo
- Flexbox para layout

## Como Executar no Expo Snack

Para rodar este projeto no [Expo Snack](https://snack.expo.dev), siga as instruções abaixo:

1. Acesse [Expo Snack](https://snack.expo.dev).
2. Copie e cole o código abaixo na janela do editor.
3. Clique em "Save" e depois em "Run" para ver o aplicativo em execução.

### Código do Projeto

```jsx
import React, { useState } from 'react';
import { View, Text, TextInput, Button, StyleSheet } from 'react-native';

export default function App() {
  const [username, setUsername] = useState('');
  const [password, setPassword] = useState('');

  const handleLogin = () => {
    // Lógica de login pode ser adicionada aqui
    alert(`Usuário: ${username}, Senha: ${password}`);
  };

  return (
    <View style={styles.container}>
      <Text style={styles.title}>Login</Text>
      <TextInput
        style={styles.input}
        placeholder="Usuário"
        value={username}
        onChangeText={setUsername}
      />
      <TextInput
        style={styles.input}
        placeholder="Senha"
        value={password}
        onChangeText={setPassword}
        secureTextEntry
      />
      <Button title="Login" onPress={handleLogin} />
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    padding: 16,
    backgroundColor: '#f0f0f0',
  },
  title: {
    fontSize: 24,
    marginBottom: 16,
    fontWeight: 'bold',
  },
  input: {
    width: '80%',
    height: 40,
    borderColor: '#ccc',
    borderWidth: 1,
    borderRadius: 4,
    paddingHorizontal: 8,
    marginBottom: 16,
    backgroundColor: '#fff',
  },
});
