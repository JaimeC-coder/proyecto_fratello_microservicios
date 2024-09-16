# Usamos una imagen base de Node.js
FROM node:20.12.0
# Establecer el directorio de trabajo
WORKDIR /app_express

# Copiar package.json y package-lock.json
COPY package*.json ./

# Instalar las dependencias
RUN npm install

# Copiar el resto del código fuente
COPY . .

# Exponer el puerto 3002 para la aplicación Express
EXPOSE 3002

# Comando para iniciar la aplicación
CMD ["npm", "start"]