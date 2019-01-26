<template>
  <div class="start_page">

    <section id="main_page">

      <form method="POST" class="start_form">

        <h1 class="start_form_title">Multicontent:</h1>
        <textarea name="urladd" rows="5" cols="100"></textarea>


        <div class="ui vertical buttons">

          <button type="send" name="action" class="ui labeled icon button" value="zadanie">
            <span class="far fa-calendar-check icon"></span>
            <span>Zadanie</span>
          </button>

          <button type="send" name="action" class="ui labeled icon button" value="wydarzenie">
            <span class="far fa-calendar icon"></span>
            <span>Wydarzenie</span>
          </button>

          <button type="send" name="action" class="ui labeled icon button" value="zakladka">
            <span class="fas fa-external-link-square-alt icon"></span>
            <span>Zakładka</span>
          </button>

          <button type="send" name="action" class="ui labeled icon button" value="notatka">
            <span class="far fa-sticky-note icon"></span>
            <span>Notatka</span>
          </button>

          <button type="send" name="action" class="ui labeled icon disabled button" value="dokument">
            <span class="far fa- icon"></span>
            <span>Dokument</span>
          </button>

          <button type="send" name="action" class="ui labeled icon disabled button" value="kontakt">
            <span class="far fa- icon"></span>
            <span>Kontakt</span>
          </button>

          <button type="send" name="action" class="ui labeled icon disabled button" value="kod/haslo">
            <span class="far fa- icon"></span>
            <span>Kod/hasło</span>
          </button>

        </div>

      </form>

      <div class="main_page_dates">

        <h1 class="start_form_title">Kalendarz:</h1>


          <div class="ui card red task" data-task="96">
            <input type="hidden" data-timer-deadline="" value="2019-02-24 12:15:00">
            <div class="content">
              <div class="header">wiązowna 5km</div>
              <div class="meta">2019-02-24 12:15:00</div>

            </div>
            <div class="extra content">
              <i class="fas fa-stopwatch"></i>
              <span type="text" name="" data-timer-output="" value="">29 Dni, 12 Godz. 8 Min. 4 Sek.</span>

            </div>
          </div>


          <div class="ui card red task" data-task="90">
            <input type="hidden" data-timer-deadline="" value="2020-06-13 21:09:00">
            <div class="content">
              <div class="header">Dominik wesele</div>
              <div class="meta">2020-06-13 21:09:00</div>

            </div>
            <div class="extra content">
              <i class="fas fa-stopwatch"></i>
              <span type="text" name="" data-timer-output="" value="">504 Dni, 20 Godz. 2 Min. 4 Sek.</span>

            </div>
          </div>


        <a class="ui button fluid" href="?page=kalendarz">Zobacz wszystkie</a>

      </div>


      <div class="main_page_dates">

        <h1 class="start_form_title">To do:</h1>


          <div class="ui card teal task" data-task="55">
            <input type="hidden" data-timer-deadline="" value="0000-00-00 00:00:00">
            <div class="content">
              <div class="header">druknąć faktury orange</div>
              <div class="meta">0000-00-00 00:00:00</div>

            </div>
            <div class="extra content">
              <i class="fas fa-stopwatch"></i>
              <span type="text" name="" data-timer-output="" value=""></span>

            </div>
          </div>


          <div class="ui card teal task" data-task="54">
            <input type="hidden" data-timer-deadline="" value="0000-00-00 00:00:00">
            <div class="content">
              <div class="header">druknać fakturę wfirma i sprawdzić resztę</div>
              <div class="meta">0000-00-00 00:00:00</div>

            </div>
            <div class="extra content">
              <i class="fas fa-stopwatch"></i>
              <span type="text" name="" data-timer-output="" value=""></span>

            </div>
          </div>


          <div class="ui card teal task" data-task="47">
            <input type="hidden" data-timer-deadline="" value="0000-00-00 00:00:00">
            <div class="content">
              <div class="header">obczaić paliwo tańsze alior</div>
              <div class="meta">0000-00-00 00:00:00</div>

            </div>
            <div class="extra content">
              <i class="fas fa-stopwatch"></i>
              <span type="text" name="" data-timer-output="" value=""></span>

            </div>
          </div>


          <div class="ui card teal task" data-task="45">
            <input type="hidden" data-timer-deadline="" value="2018-12-02 20:00:00">
            <div class="content">
              <div class="header">Adrenalina poprawki z maila 21.11</div>
              <div class="meta">2018-12-02 20:00:00</div>

            </div>
            <div class="extra content error">
              <i class="fas fa-stopwatch"></i>
              <span type="text" name="" data-timer-output="" value="">-55 Dni, -5 Godz. -7 Min. -56 Sek.</span>

            </div>
          </div>


          <div class="ui card teal task" data-task="44">
            <input type="hidden" data-timer-deadline="" value="0000-00-00 00:00:00">
            <div class="content">
              <div class="header">ściągnąć 2 faktury za aruba cloud</div>
              <div class="meta">0000-00-00 00:00:00</div>

            </div>
            <div class="extra content">
              <i class="fas fa-stopwatch"></i>
              <span type="text" name="" data-timer-output="" value=""></span>

            </div>
          </div>


        <a class="ui button fluid" href="?page=do-zrobienia">Zobacz wszystkie</a>

      </div>


      <pre>    <span>javascript:(function(){var win = window.open('http://studiocitrus.pl/datownik/?urladd='+window.location.href, '_blank'); win.focus();})();</span>
      </pre>
      <pre>    Current PHP version: 5.6.35  </pre>
      <pre>    https://stackoverflow.com/questions/18377891/how-can-i-let-user-paste-image-data-from-the-clipboard-into-a-canvas-element-in
      </pre>
      <pre>    do code snippetów -
        https://codepen.io/chriscoyier/pen/GBbOJd
      </pre>

    </section>

    <StartPageNotes/>

  </div>
</template>

<script>
import StartPageNotes from './start_page_notes.vue';
export default {
  name: 'StartPage',
  components: {
    StartPageNotes,
  },
  props: {
    msg: String
  }
}
</script>

<style scoped>

</style>
