# Usar la imagen base de Node.js
FROM node:20.12.0 as dev

# Crear y establecer el directorio de trabajo
RUN mkdir /project
WORKDIR /project

# Instalar Angular CLI globalmente (con la versión correcta)
RUN npm install -g @angular/cli@17.3.4

# Copiar los archivos de dependencias
COPY package.json package-lock.json ./

# Instalar dependencias
RUN npm ci

# Copiar el resto del código del proyecto
COPY . .

# Exponer el puerto 4200
EXPOSE 4200

# Comando para iniciar la aplicación en modo desarrollo
CMD ["ng", "serve", "--host", "0.0.0.0"]
