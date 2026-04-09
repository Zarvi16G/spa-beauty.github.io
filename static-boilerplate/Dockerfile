# Etapa 1: Construcción (Build)
FROM node:18-alpine AS build-stage

# Crear directorio de trabajo
WORKDIR /app

# Copiar archivos de dependencias primero para aprovechar el caché de Docker
COPY package*.json ./

# Instalar dependencias
RUN npm install

# Copiar el resto del código y compilar
COPY . .

# Exponer el puerto 80
EXPOSE 5173

CMD ["npm", "run", "dev"]