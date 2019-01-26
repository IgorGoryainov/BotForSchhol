# -*- coding: utf-8 -*-
import vk_api
import time
import datetime
soob = ''
d1 = '1. Электив(матан) \n 2. Литература \n 3. Английский язык \n 4. Биология \n 5. Математика \n 6. Математика'
d2 = '1. Инф(гр1)/Ино(гр2) \n 2. История \n 3. ОБЖ \n 4. Геометрия \n 5. Ино(гр1)/Инф(гр2) \n 6. Физика'
d3 = '1. Сон \n 2. Алгебра \n 3. Обществознание \n 4. Обществознания \n 5. Литература \n 6. Астрономия'
d4 = '1. Электив(матан) \n 2. Химия \n 3. Физика \n 4. Физ - ра \n 5. История \n 6. Английский язык'
d5 = '1. Сон \n 2. Литература \n 3. Геометрия \n 4. Геометрия \n 5. Русский язык \n 6. Физкультра'
d6 = '1. Алгебра \n 2. Физика \n 3. Алгебра \n 4. Физкультура \n 5. Физика \n 6. Русский язык \n 7. Физика'
d7 = 'Воскресенье'
masw = ['monday.txt', 'tuesday.txt', 'wednesday.txt', 'thursday.txt', 'friday.txt', 'saturday.txt']
def numberweek():
    numberw = (datetime.datetime.utcnow().isocalendar()[1])
    return numberw
def boardtoday():
    dayweek = (time.strftime('%w', time.localtime()))
    dw = int(dayweek)
    if dw == 1:
        d = d1
    elif dw == 2:
        d = d2
    elif dw == 3:
        d = d3
    elif dw == 4:
        d = d4
    elif dw == 5:
        d = d5
    elif dw == 6:
        d = d6
    elif dw == 0:
        d = d7
    return(d)
def boardtomorow():
    dayweek = (time.strftime('%w', time.localtime()))
    dw = int(dayweek)
    if dw == 1:
        d = d2
    elif dw == 2:
        d = d3
    elif dw == 3:
        d = d4
    elif dw == 4:
        d = d5
    elif dw == 5:
        d = d6
    elif dw == 6:
        d = "Домашнее задание на понедельник: \n " + d1
    elif dw == 0:
        d = d1
    return(d)
def pish(dn):
    if dn == 1:
        ss = str(masw[0])
    elif dn == 2:
        ss = str(masw[1])
    elif dn == 3:
        ss = str(masw[2])
    elif dn == 4:
        ss = str(masw[3])
    elif dn == 5:
        ss = str(masw[4])
    elif dn == 6:
        ss = str(masw[5])
    return(ss)
def dztoday():
    dayweek = (time.strftime('%w', time.localtime()))
    dw = int(dayweek)
    if dw != 0:
        m = pish(dw)
    else:
        m = pish(1)
    return(m)
def dztomorow():
    dayweek = (time.strftime('%w', time.localtime()))
    dw = int(dayweek)
    if dw != 6:
        m = pish(dw+1)
    else:
        m = pish(1)
    return(m)
f = open('idbase.txt', 'r')
t = f.readlines()
dz = open('dzsend.txt', 'r')
t1 = dz.readlines()
allpersondz = t1[0]
allperson = t[0]
dbi = []
timelabel = []
dzsend = []
boardsend = []
for num in range(1, int(allperson)+1):
    dbi.append(int(t[num]))
for num3 in range(1, int(allpersondz)+1):
    dzsend.append(int(t1[num3]))
f.close()
dz.close()
bs = open('boardsend.txt', 'r')
t2 = bs.readlines()
allpersonbd = t2[0]
for num5 in range(1, int(allpersonbd)+1):
    boardsend.append(int(t2[num5]))
bs.close()
token = "3260ff8cd54b8061f8b196a9e1ed52765e82b9e8677f75927a4342c6407c3c3ccf75cb014d7a61eb7587b"
vk = vk_api.VkApi(token=token)
vk._auth_token()
msg1 = 'Привет! Ты добавлен в список учеников 11А класса школы №63 г.о.Самара. Этот бот создан для того, чтобы ты больше не спамил беседу такими вопросами как: "Что задали?", "Что по алгебре? и т.д. . Бот находится в стадии разработки, поэтому функционал ограничен, не стоит добавлять бота в ЧС. Надеюсь вскором времени он тебе понравится. Расскажу коротко о том, что может сделать бот. Бот может: сказать расписание на завтра, сказать дз на завтра (при подписке на рассылку, дз на завтра будет рассылаться ежедневно), сделать напоминание о изменениях, классных событиях и т.д. (напоминания напишут за тебя, как и дз). Через неделю список функций будет расширен. Вскоре будут добавлены кнопки и бот будет сверять дз с АСУ РСО автоматически, таким образом, при резких изменениях в дз, ты будешь оповещен. Напиши "help", чтобы понять, как начать пользоваться ботом'
msg2 = 'Напиши мне цифру, соответсвующую необходимой для тебя функции:\n \n БЛОК ПОДПИСОК \n \n 1. Подписаться на ежедневную рассылку дз \n 2. Отписаться от описанной функции выше \n 3. Подписаться на ежедневную рассылку расписания, изменений и напоминаний на следующий день. Через пробел указать время в которое удобно получать рассылку. Пример: 3 18 30. Это значит, что бот тебе будет отправлять рассылку в 18:30  \n 4. Отписаться от описанной функции выше \n \n БЛОК КОМАНД \n \n 5. Скажи дз на сегодня \n 6. Скажи дз на завтра \n 7. Скажи расписание на сегодня \n 8. Скажи расписание на завтра \n 9. Пришли интернет-ссылки на наши учебники'
msg3 = 'Литература: http://rabochaya-tetrad-uchebnik.com/literatura/literatura_11_klass_uchebnik_kurdyumova_chastj_1/index.html#prettyPhoto[gallery3]/48/ \n Алгебра задачник: http://rabochaya-tetrad-uchebnik.com/algebra/uchebnik_algebra_11_klass_zadachnik_mordkovich_chastj_2_profiljnyy_urovenj/index.html \n Алгебра учебник: http://rabochaya-tetrad-uchebnik.com/algebra/algebra_11_klass_uchebnik_mordkovich_semenov_chastj_1/index.html \n Физика Марон: http://fizmatege.ru/wp-content/uploads/2015/08/370_3-%D0%A4%D0%B8%D0%B7%D0%B8%D0%BA%D0%B0.-11%D0%BA%D0%BB.-%D0%94%D0%B8%D0%B4%D0%B0%D0%BA%D1%82.-%D0%BC%D0%B0%D1%82%D0%B5%D1%80._%D0%9C%D0%B0%D1%80%D0%BE%D0%BD_2014-144%D1%81-1.pdf \n Глизбург Алгебра: https://vk.com/away.php?to=https%3A%2F%2Fdownloader.disk.yandex.ru%2Fdisk%2F52180903c213ba2475e6bf2e9f66e35d11a187bb82db79f6412f6a31aa564535%2F5c44e93a%2FTMHMM03-hqWccsoQ9_lNOlEx9skwKILxY0lw_DqdTR-EaB38lMWiDZjYfjk6NlwX6cdX1uUC6tcUJm4aQ69WZw%253D%253D%3Fuid%3D0%26filename%3D671.pdf%26disposition%3Dattachment%26hash%3Dy4UjDV5FygET%2F1Hc9%2FvxHvhmKrEJWw0kKKqdOmxRZzI%253D%26limit%3D0%26content_type%3Dapplication%252Fpdf%26fsize%3D525380%26hid%3Dc0a409477418d832805220b9b36f30bb%26media_type%3Ddocument%26tknv%3Dv2&cc_key= \n История: http://rabochaya-tetrad-uchebnik.com/istoriya/uchebnik_istoriya_rossiya_i_mir_11_klass_bazovyy_urovenj_volobuev_klokov/index.html \n Русский язык: http://rabochaya-tetrad-uchebnik.com/russkiy_yazyk/uchebnik_russkiy_yazyk_10-11_klass_goljcova_shamshin_mishherina_chastj_2/index.html'
while True:
    try:
        messages = vk.method("messages.getConversations", {"offset": 0, "count": 20, "filter": "unanswered"})
        if messages["count"] >= 1:
            id = messages["items"][0]["last_message"]["from_id"]
            body = messages["items"][0]["last_message"]["text"]
            msglist = list(body.lower())
            if body.lower() == "sending000":
                for num1 in range(len(dbi)):
                    vk.method("messages.send", {"peer_id": dbi[num1], "message": msg1})
            elif body.lower() == "sendingdz":
                t3 = dztomorow()
                k3 = open(t3, 'r')
                k4 = k3.readlines()
                k3.close()
                for nums in range(len(dzsend)):
                    vk.method("messages.send", {"peer_id": dzsend[nums], "message": "Домашнее задание на завтра: \n \n" + str(k4[1])})
            elif body.lower() == "sendingboard":
                dos = boardtomorow()
                for numsi in range(len(boardsend)):
                    vk.method("messages.send", {"peer_id": boardsend[numsi], "message": "Расписание на завтра: \n \n" + dos})
            elif body.lower() == "sendingall":
                t3 = dztomorow()
                k3 = open(t3, 'r')
                k4 = k3.readlines()
                k3.close()
                dos = boardtomorow()
                for numsic in range(len(boardsend)):
                    vk.method("messages.send", {"peer_id": dbi[numsic], "message": "Домашнее задание на завтра: \n \n" + str(k4[1]) + "\n \n" + "Расписание на завтра: \n \n" + dos + "\n \n" + "Подпишись на рассылки (1 и 3)! Данная рассылка была произведена не по подпискам. Прост мало в БД подписок, а это плохо((( "})
            elif body.lower() == "sendingall1":
                t3 = dztomorow()
                k3 = open(t3, 'r')
                k4 = k3.readlines()
                k3.close()
                dos = boardtomorow()
                for numsic in range(len(boardsend)):
                    vk.method("messages.send", {"peer_id": dbi[numsic], "message": "Привет! Обновлен список функций. Напишите цифру 9, чтобы получить ссылки на учебники, если вы их забыли дома. Можете просто написать help, чтобы чекнуть все функции "})
            elif body.lower() == "help":
                vk.method("messages.send", {"peer_id": id, "message": msg2})
            elif body.lower() == "1":
                if dzsend.count(id) == 0:
                    vk.method("messages.send", {"peer_id": id, "message": 'Подписка оформлена. Теперь каждый день я тебе буду присылать дз.'})
                    dzsend.append(id)
                else:
                    vk.method("messages.send", {"peer_id": id, "message": 'Ты уже подписан.'})

            elif body.lower() == "2":
                if dzsend.count(id) == 1:
                    vk.method("messages.send", {"peer_id": id, "message": 'Так жаль... Потом скажешь почему отписался.'})
                    dzsend.remove(id)
                else:
                    vk.method("messages.send", {"peer_id": id, "message": 'Так ты и не подписан'})
            elif msglist[0] == "3":
                if boardsend.count(id) == 0:
                    tchas = msglist[1]
                    tmin = msglist[2]
                    boardsend.append(id)
                    timelabel.append(id)
                    timelabel.append(tchas)
                    timelabel.append(tmin)
                    vk.method("messages.send", {"peer_id": id, "message": "Подписка оформлена"})
                else:
                    vk.method("messages.send", {"peer_id": id, "message": 'Ты уже подписан.'})
            elif body.lower() == "4":
                if boardsend.count(id) == 1:
                    vk.method("messages.send", {"peer_id": id, "message": 'Так жаль... Потом скажешь почему отписался.'})
                    boardsend.remove(id)
                else:
                    vk.method("messages.send", {"peer_id": id, "message": 'Так ты и не подписан'})
            elif body.lower() == "7":
                do = boardtoday()
                vk.method("messages.send", {"peer_id": id, "message": do})
            elif body.lower() == "8":
                do1 = boardtomorow()
                vk.method("messages.send", {"peer_id": id, "message": do1})
            elif body.lower() == "5":
                t1 = dztoday()
                k1 = open(t1, 'r')
                k2 = k1.readlines()
                k1.close()
                vk.method("messages.send", {"peer_id": id, "message": str(k2[1])})
            elif body.lower() == "6":
                t3 = dztomorow()
                k3 = open(t3, 'r')
                k4 = k3.readlines()
                k3.close()
                vk.method("messages.send", {"peer_id": id, "message": str(k4[1])})
            elif body.lower() == "9":
                vk.method("messages.send", {"peer_id": id, "message": msg3})
            elif len(msglist) > 6:
                if (msglist[0] + msglist[1] + msglist[2]) == "101":
                    dzs = ''
                    dn = int(msglist[4])
                    dzn = len(msglist)
                    m = pish(dn)
                    l55 = open(m, 'r')
                    l551 = l55.readlines()
                    l55.close()
                    for num16 in range(5, dzn):
                        dzs += msglist[num16]
                    l551.append(dzs)
                    m1 = open(m, 'w')
                    nn = len(l551)
                    m1.write(str(l551[0]))
                    for ni in range(1, nn):
                        m1.write(str(l551[ni]) + " ;")
                    m1.close()
                    vk.method("messages.send", {"peer_id": id, "message": str(dzs)})
                    del(dzs)
                    l551.clear()
                else:
                    pass
                continue
            else:
                if dbi.count(id) == 0:
                    vk.method("messages.send", {"peer_id": id, "message": msg1})
                    dbi.append(id)
                else:
                    vk.method("messages.send", {"peer_id": id, "message": "Я не понимаю тебя. Ввел что-то неправильно."})
            f1 = open("idbase.txt", 'w')
            f1.write(str(len(dbi))+"\n")
            for num2 in range(len(dbi)):
                f1.write(str(dbi[num2])+"\n")
            f1.close()
            dz1 = open('dzsend.txt', 'w')
            dz1.write(str(len(dzsend))+"\n")
            for num4 in range(len(dzsend)):
                dz1.write(str(dzsend[num4])+"\n")
            dz1.close()
            bs1 = open('boardsend.txt', 'w')
            bs1.write(str(len(boardsend))+"\n")
            for num6 in range(len(boardsend)):
                bs1.write(str(boardsend[num6])+"\n")
            bs1.close()
            numberw = (datetime.datetime.utcnow().isocalendar()[1])
            l1 = open('monday.txt', 'r')
            l2 = l1.readlines()
            l1.close()
            if int(l2[0]) != int(numberw):
                l5 = open('monday.txt', 'w')
                l6 = open('tuesday.txt', 'w')
                l6.write(str(numberw) + "\n")
                l5.write(str(numberw) + "\n")
                l7 = open('wednesday.txt', 'w')
                l7.write(str(numberw) + "\n" )
                l8 = open('thursday.txt', 'w')
                l8.write(str(numberw) + "\n")
                l9 = open('friday.txt', 'w')
                l9.write(str(numberw)+ "\n")
                l10 = open('saturday.txt', 'w')
                l10.write(str(numberw) + "\n")
                l5.close()
                l6.close()
                l7.close()
                l8.close()
                l9.close()
                l10.close()
            soob = ''
    except Exception as E:
        time.sleep(1)

