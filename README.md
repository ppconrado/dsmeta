## Objetivos do projeto fase 1

- Criar projetos backend e frontend
- Salvar os projeto no Github em monorepo
- Montar o visual estático do front end

# Checklist

## Design Figma

https://www.figma.com/file/PehiT8Dw4Lv5ioTSULZeRI/DSMeta3

https://www.figma.com/file/Yu2RHFmirHQ4BIVZM2XxY6/DSMeta2

https://www.figma.com/file/EN1zFtk4eY3Jgmpgi9YaMG/DSMeta1

## Ferramentas

- Nodejs 16 e Yarn (vídeo: https://youtu.be/x5tgFTS-CYA )
- STS (vídeo: https://youtu.be/TGQ0K9QsX88 )
- VS Code
  - `IntelliCode`
  - `ESLint`
  - `JSX HTML <tags/>`

## Passo: criar projeto ReactJS

![ppconrado github img](https://raw.githubusercontent.com/ppconrado/bds-assets/master/sds/pastas-dsmeta.png)

```
yarn create vite frontend --template react-ts
```

## Passo: criar projeto Spring Boot

- Criar projeto Spring Boot no `Spring Initializr` com as seguintes dependências:

  - Web
  - JPA
  - H2
  - Security

- Ajuste no arquivo pom.xml:

```xml
<plugin>
	<groupId>org.apache.maven.plugins</groupId>
	<artifactId>maven-resources-plugin</artifactId>
	<version>3.1.0</version><!--$NO-MVN-MAN-VER$ -->
</plugin>
```

- Botão direito no projeto -> Maven -> Update project (force update)

```bash
git init

git add .

git commit -m "Project created"

git branch -M main

git remote add origin git@github.com:seuusuario/seurepositorio.git

git push -u origin main
```

## Passo: "limpar" o projeto ReactJS

## Passo: Datepicker

Documentação: https://github.com/Hacker0x01/react-datepicker

```
yarn add react-datepicker@4.8.0 @types/react-datepicker@4.4.2
```

```javascript
import DatePicker from "react-datepicker";
import "react-datepicker/dist/react-datepicker.css";
```

```javascript
<DatePicker
  selected={new Date()}
  onChange={(date: Date) => {}}
  className="dsmeta-form-control"
  dateFormat="dd/MM/yyyy"
/>
```

## Passo: React Hook useState para manter estado das datas

Para criar uma data de X dias atrás:

```javascript
const date = new Date(new Date().setDate(new Date().getDate() - 365));
```
