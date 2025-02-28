# Проект pars
Информационная система для сопровождения учебого процесса по программированию
<h2 dir="auto"><a id="user-content-описание-проекта" class="anchor" aria-hidden="true" href="#описание-проекта"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Описание проекта</h2>
Проект разработан по заказу Бурятского государственного университета имени Доржи Банзарова. 
Использование информационной системы позволит ускорить сбор и анализ данных о прогрессе обучающихся на веб-ресурсе <a href="https://acmp.ru">acmp.ru</a>. В следствие чего использование информационной системы позволит преподавателю существенно экономить рабочее время про работе с большими группами учеников. 
Проект преимущественно написан на языке Python с использованием фреймворка Django, работа с базой данных реализованна с использованием СУБД PostgreSQL.


<h2 dir="auto"><a id="user-content-описание-проекта" class="anchor" aria-hidden="true" href="#описание-проекта"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg><h2>Модели системы</h2>

Классы:
<ul>
     <li><code>User</code> класс для работы с пользователями </li>
     <li><code>Group</code> класс для работы с группами обучающихся </li>
     <li><code>TaskAcmp</code> класс для работы с тематическими подборками задач </li>
     <li><code>Student</code> класс для работы с данными обучающихся </li>
</ul>
<h2 dir="auto"><a id="user-content-описание-проекта" class="anchor" aria-hidden="true" href="#описание-проекта"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg><h2>Основные действия осуществляются следующими представлениями</h2>
<b> Представления для работы с группой </b>
<ul>
     <li><code>groups_home(request)</code> представление выводит полный список групп преподавателя </li>
     <li><code>selected_group(request, pk)</code> представление выводит список обучающихся в группе с идентификатором pk</li>
     <li><code>add_group(request)</code> представление для создания новой группы</li>
     <li><code>edit_group(UpdateView)</code> представление для редактирования информации о выбранной группе</li>
     <li><code>delete_group(DeleteView)</code> представление для удаления выбранной группы. При удалении группы все обучающиеся находящиеся в группе так же удаляются </li>
</ul>
<b> Представления для работы с тематическими подборками задач </b>
<ul>
     <li><code>task_home(request)</code> представление выводит полный список подборок задач преподавателя</li>
     <li><code>add_task(request)</code> представление для создания новой подборки задач</li>
     <li><code>edit_task(UpdateView)</code> представление для редактирования выбранной подборки задач</li>
     <li><code>delete_task(DeleteView)</code> представление для удаления выбранной подборки задач</li>
</ul>
<b> Представления для работы с обучающимися </b>
<ul>
     <li><code>add_student(request, pk)</code> представление для создания нового обучающегося в группе с идентификатором pk</li>
     <li><code>edit_student(UpdateView)</code> представление для редактирования информации о выбранном обучающемся</li>
     <li><code>delete_student (DeleteView)</code> представление для удаления обучающегося</li>
     <li><code>student_statistic(request, pk)</code> представление для анализа прогресса обучающегося с идентификатором pk</li>
     <li><code>update_parse(requests, pk)</code> представление для получения данных с веб-ресурса acmp.ru об обучающемся с идентификатором pk</li>
</ul>
