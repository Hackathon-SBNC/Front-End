<script setup>
    import DesktopOldOccurence from './DesktopOldObservation.vue'
</script>

<template>
    <div class="container">
        <div class="form">
        <div class="ocorrencia">
            <label for="ocurrence">
                <h1>Observações</h1>
            </label>

            <textarea rows="" cols=""></textarea>
        </div>

        <div class="acoes">
            <h1>Ação a ser feita</h1>

            <div class="options">
                <span class="check-container">
                    <input type="checkbox" id="family-school" class="check-texto" />
                    <label for="family-school" class="check-customizado"></label>
                    <label for="family-school">Reunião Família Escola</label>
                </span>
                <span class="check-container">
                    <input type="checkbox" id="study-club" class="check-texto" />
                    <label for="study-club" class="check-customizado"></label>
                    <label for="study-club">Participação em Grupo de Estudo</label>
                </span>
                <span class="check-container">
                    <input type="checkbox" id="sisae" class="check-texto" />
                    <label for="sisae" class="check-customizado"></label>
                    <label for="sisae">Reunião SISAE</label>
                </span>
                <span class="check-container">
                    <input type="checkbox" id="course" class="check-texto" />
                    <label for="course" class="check-customizado"></label>
                    <label for="course">Reunião Coordenação de Curso</label>
                </span>
            </div>
        </div>
        </div>

        <DesktopOldOccurence />
        
    </div>
</template>

<style scoped>
textarea {
  height: 100%;
  width: calc(100% - 2rem);
  resize: none;
  border-color: var(--gray);
  border-radius: 1rem;
  outline: none;
  padding: 1rem;
}

h1{
    margin: 0;
}

.options{
    display: flex;
    flex-direction: column;
    gap: 2vh;

}
    .check-container {
        display: flex;
        gap: 0.8vw;
        align-items: center;
 

        & input {
          display: none;
        }

        & input:checked + .check-customizado {
          background-color: var(--green);
        }

        .check-customizado {
          display: relative;
          width: 15px;
          height: 15px;
          border: 1px solid var(--green);
          display: inline;
        }
    }

    .acoes{
        width: 30vw;
        display: flex;
        flex-direction: column;
        gap: 4vh;
        padding: 4vh 1vw;
    }

    .container {
        padding: 1%;
        margin: auto;
        display: flex;
        flex-direction: column;
        width: 50vw;
        height: auto;
        color: var(--black);
        border: 1px solid var(--gray);
        border-radius: 10px;
    }

    .ocorrencia {
        width: 65%;
        display: flex;
        flex-direction: column;
        gap: 4vh;
        padding: 4vh 1vw;
        & input {
            display: flex;
            justify-self: center;
            width: 95%;
            height: 32vh;
            border: 1px solid var(--gray);
            border-radius: 10px;
        }

        & input:focus {
            outline: none;
        }
    }

    .form {
        display: flex;
    }
</style>