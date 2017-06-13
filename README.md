# pythonTicTacToeAI
TicTacToe with AI in python
def imprimirtabuleiro():
    i=0
    j=0
    print("                 -------------")
    while i<3:
        print "                ",
        while j<3:
            print "|",
            print tab[i][j],
            j=j+1
        print "|",
        i=i+1
        j=0
        print
        if i<=2:
            print("                 ----+---+----")
        else:
            print("                 -------------")
def jogar(jogador):
    p=1
    while p==1:
        jogada=input("  Humano %s digite o numero da jogada: "%(jogador))
        jogada=jogada-1
        if type(tab[jogada/3][jogada%3])==int:
            tab[jogada/3][jogada%3]=jogador
            p=0
        else:
            print("  Jogada ja efetuada, jogue novamente")
def checarvitoria(jogador):
    if tab[0].count(jogador)==3 or tab[1].count(jogador)==3 or tab[2].count(jogador)==3:
        if (primeiro==1 and jogador==x) or (primeiro!=1 and jogador==o) or primeiro==0:
            print("  Parabens senhor humano %s, voce ganhou! "%(jogador))
        else:
            print("  AI ganhou o jogo, boa sorte na proxima vez humano")
        return(0)
    if tab[0][0]==jogador and tab[1][0]==jogador and tab[2][0]==jogador:
        if (primeiro==1 and jogador==x) or (primeiro!=1 and jogador==o) or primeiro==0:
            print("  Parabens senhor humano %s, voce ganhou! "%(jogador))
        else:
            print("  AI ganhou o jogo, boa sorte na proxima vez humano")
        return(0)
    if tab[0][1]==jogador and tab[1][1]==jogador and tab[2][1]==jogador:
        if (primeiro==1 and jogador==x) or (primeiro!=1 and jogador==o) or primeiro==0:
            print("  Parabens senhor humano %s, voce ganhou! "%(jogador))
        else:
            print("  AI ganhou o jogo, boa sorte na proxima vez humano")
        return(0)
    if tab[0][2]==jogador and tab[1][2]==jogador and tab[2][2]==jogador:
        if (primeiro==1 and jogador==x) or (primeiro!=1 and jogador==o) or primeiro==0:
            print("  Parabens senhor humano %s, voce ganhou! "%(jogador))
        else:
            print("  AI ganhou o jogo, boa sorte na proxima vez humano")
        return(0)
    if tab[0][0]==jogador and tab[1][1]==jogador and tab[2][2]==jogador:
        if (primeiro==1 and jogador==x) or (primeiro!=1 and jogador==o) or primeiro==0:
            print("  Parabens senhor humano %s, voce ganhou! "%(jogador))
        else:
            print("  AI ganhou o jogo, boa sorte na proxima vez humano")
        return(0)
    if tab[0][2]==jogador and tab[1][1]==jogador and tab[2][0]==jogador:
        if (primeiro==1 and jogador==x) or (primeiro!=1 and jogador==o) or primeiro==0:
            print("  Parabens senhor humano %s, voce ganhou! "%(jogador))
        else:
            print("  AI ganhou o jogo, boa sorte na proxima vez humano")
        return(0)
    else:
        return(1)
def ai(jogador,adversario):
    z=0
    contarcoluna=[0,0,0]
    if type(tab[1][1])==int:
        tab[1][1]=jogador
        print("AI: HAHA, essa vitoria esta no papo!")
        z=1
    else:
        i=0
        while i<3 and z==0:
            if tab[i].count(jogador)==2 and z==0:
                if type(tab[i][0])==int and z==0:
                    tab[i][0]=jogador
                    print("AI: Ufa, consegui")
                    z=1
                if type(tab[i][1])==int and z==0:
                    tab[i][1]=jogador
                    print("AI: Treinei muito para esse momento")
                    z=1
                if type(tab[i][2])==int and z==0:
                    tab[i][2]=jogador
                    print("AI: Ganhei de olhos fechados")
                    z=1
            if tab[0][i]==jogador and z==0:
                contarcoluna[i]=contarcoluna[i]+1
            if tab[1][i]==jogador and z==0:
                contarcoluna[i]=contarcoluna[i]+1
            if tab[2][i]==jogador and z==0:
                contarcoluna[i]=contarcoluna[i]+1
            i=i+1
        i=0
        while i<3 and z==0:
            if contarcoluna[i]==2 and z==0:
                if type(tab[0][i])==int and z==0:
                    tab[0][i]=jogador
                    print("AI: Nossa, que minha vovo ficaria orgulhosa")
                    z=1
                if type(tab[1][i])==int and z==0:
                    tab[1][i]=jogador
                    print("AI: VOZINHA! vem ver esse humano")
                    z=1
                if type(tab[2][i])==int and z==0:
                    tab[2][i]=jogador
                    print("AI: GGWP")
                    z=1
            i=i+1
        if tab[0][0]==jogador and tab[1][1]==jogador and type(tab[2][2])==int and z==0:
            tab[2][2]=jogador
            print("AI: Que coisa nao ?!")
            z=1
        if tab[1][1]==jogador and tab[2][2]==jogador and type(tab[0][0])==int and z==0:
            tab[0][0]=jogador
            print("AI: Pega a camera vovoooo, nao, pera")
            z=1
        if tab[0][2]==jogador and tab[1][1]==jogador and type(tab[2][0])==int and z==0:
            tab[2][0]=jogador
            print("AI: Best AI WORLD")
            z=1
        if tab[1][1]==jogador and tab[2][0]==jogador and type(tab[0][2])==int and z==0:
            tab[0][2]=jogador
            print("AI: Quem diria hein?!")
            z=1   
        i=0
        contarcoluna=[0,0,0]
        while i<3 and z==0:
            if tab[i].count(adversario)==2 and z==0:
                if type(tab[i][0])==int and z==0:
                    tab[i][0]=jogador
                    print("AI: Jamais ira ganhar")
                    z=1
                if type(tab[i][1])==int and z==0:
                    tab[i][1]=jogador
                    print("AI: Nao dessa forma")
                    z=1
                if type(tab[i][2])==int and z==0:
                    tab[i][2]=jogador
                    print("AI: Nao contavam com minha astucia")
                    z=1
            if tab[0][i]==adversario and z==0:
                contarcoluna[i]=contarcoluna[i]+1
            if tab[1][i]==adversario and z==0:
                contarcoluna[i]=contarcoluna[i]+1
            if tab[2][i]==adversario and z==0:
                contarcoluna[i]=contarcoluna[i]+1
            i=i+1
        i=0
        while i<3:
            if contarcoluna[i]==2 and z==0:
                if type(tab[0][i])==int and z==0:
                    tab[0][i]=jogador
                    print("AI: Nao deixarei que isso aconteca")
                    z=1
                if type(tab[1][i])==int and z==0:
                    tab[1][i]=jogador
                    print("AI: Opa, quaseeeee")
                    z=1
                if type(tab[2][i])==int and z==0:
                    tab[2][i]=jogador
                    print("AI: Quase nao vi essa jogada")
                    z=1
            i=i+1
        if tab[0][0]==adversario and tab[1][1]==adversario and type(tab[2][2])==int and z==0:
            tab[2][2]=jogador
            print("AI: Achou que eu nao perceberia, neh ?!")
            z=1
        if tab[1][1]==adversario and tab[2][2]==adversario and type(tab[0][0])==int and z==0:
            tab[0][0]=jogador
            print("AI: Nada escapa os meus olhos")
            z=1
        if tab[0][2]==adversario and tab[1][1]==adversario and type(tab[2][0])==int and z==0:
            tab[2][0]=jogador
            print("AI: Voce queria esse espaco neh?! Que pena")
            z=1
        if tab[1][1]==adversario and tab[2][0]==adversario and type(tab[0][2])==int and z==0:
            tab[0][2]=jogador
            print("AI: Unnnn , nao enquanto eu estiver aqui")
            z=1
        if z==0:
                if type(tab[0][0])==int and z==0:
                    if tab[0][2]==adversario and tab[2][0]==adversario:
                        pass
                    else:
                        if tab[2][1]==adversario and tab[1][2]==adversario:
                            pass
                        else:
                            tab[0][0]=jogador
                            print("AI: Minha jogada de mestre")
                            z=1
                if type(tab[0][2])==int and z==0:
                    if tab[0][0]!=adversario and tab[2][0]!=adversario:
                        tab[0][2]=jogador
                        print("AI: Minha jogada de mestre")
                        z=1
                if type(tab[2][0])==int and z==0:
                    if tab[0][2]!=adversario and tab[0][0]!=adversario:
                        tab[2][0]=jogador
                        print("AI: Minha jogada de mestre")
                        z=1
                if type(tab[2][2])==int and z==0:
                    if tab[0][2]!=adversario and tab[2][0]!=adversario:
                        tab[2][2]=jogador
                        print("AI: Minha jogada de mestre")
                        z=1
                if type(tab[0][1])==int and z==0:
                    tab[0][1]=jogador
                    print("AI: Best jogada")
                    z=1
                if type(tab[1][0])==int and z==0:
                    tab[1][0]=jogador
                    print("AI: Best jogada")
                    z=1
                if type(tab[1][2])==int and z==0:
                    tab[1][2]=jogador
                    print("AI: Best jogada")
                    z=1
                if type(tab[2][1])==int and z==0:
                    tab[2][1]=jogador
                    print("AI: Best jogada")
                    z=1
                c1=0
                c2=0
                while z==0 and c1<3:
                    while z==0 and c2<3:
                        if type(tab[c1][c2])==int and z==0:
                            tab[c1][c2]=jogador
                            z=1
                            print("AI: eh isso ja deu vovozinha")
                        c2=c2+1
                    c2=0
                    c1=c1+1                    
def geratabuleiro():
    i=0
    j=0
    num=1
    while i<3:
        tab.append([])
        while j<3:
            tab[i].append(num)
            num=num+1
            j=j+1
        j=0
        i=i+1
print("           Bem-vindo ao Jogo da velha")
novamente=1
while novamente==1:
    tab=[]
    x="X"
    o="O"
    primeiro=0
    geratabuleiro()
    imprimirtabuleiro()
    print("     Digite 8                     Digite 9 ")
    modo=input("  Para jogar vs Ai          Para Jogar vs Humano: ")
    if modo==8:
        print
        print("     Digite 1                     Digite 2 ")
        primeiro=input("  Deseja comecar ?          Deseja que Ai comece ? ")
    loop=1
    while loop==1:
        if primeiro==1 or modo!=8:
            jogar(x)
        else:
            ai(x,o)
        imprimirtabuleiro()
        cx=checarvitoria(x)
        if (tab[0].count(x)+tab[1].count(x)+tab[2].count(x)==5) and cx==1:
            loop=0
            print("  Houve empate")
        if cx==1 and loop==1:
            if primeiro==1:
                ai(o,x)
            else:
                jogar(o)
            imprimirtabuleiro()
            co=checarvitoria(o)
            if co==0:
                loop=0
        if cx==0:
            loop=0
    print("  Deseja jogar novamente ?")
    novamente=input("  Digite 1 para sim e 0 para nao: ")
