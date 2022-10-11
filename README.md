# Criando Docker Image com Buildpacks

##### Adicionar:
##### Observação: O nome da imagem alí está apenas como exemplo.
````
<plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
                <configuration>
                    <image>
                        <name>tuyosistema/${project.artifactId}</name>
                    </image>
                </configuration>
            </plugin>
</plugins>
````

### Rodar o comando dentro do diretório com o pom.xml, que usa buildpacks, para gerar uma imagem docker para o projeto:
````
mvn spring-boot:build-image
````
### Depois de rodar o comando acima dentro do diretório em que se encontra o pom.xml, ele fará o pull das imagens do repositório do DockerHub e isso ajudará a criar imagens baseadas no conceito de buildpacks.

### Imagem criada: Successfully built image 'docker.io/tuyosistema/loansdockerize:latest'

# O nome da imagem foi colocado aqui:
````
    <image>
        <name>tuyosistema/${project.artifactId}</name>
    </image>
````

# Imagem feita sem dockerfile, ou seja, sem as definicoes do mesmo.
