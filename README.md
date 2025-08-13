# Use-effect
Projeto senai
import { useState, useEffect } from 'react';

function MeuComponente() {
  const [dados, setDados] = useState([]);

  useEffect(() => {
    fetch('https://api.example.com/dados')
      .then(response => response.json())
      .then(data => setDados(data));
  }, []);

  return (
    <div>
      {dados.map(item => (
        <p key={item.id}>{item.nome}</p>
      ))}
    </div>
  );
}
