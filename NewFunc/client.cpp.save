//{===========================================================================
//! @file       Examples/Example04/client.cpp
//!
//! @brief      Четвертый пример использования TXNetwork - много шариков.
//!
//!             Библиотека Сети Тупых Художников (TXNetwork).
//!
//!             Синхронные шарики на многих компьютерах c использованием broadcast'a и UDP.
//!
//!             $Copyright: (C) _RedMan_ (Vova Yrovsky) <vova@txlib.ru> $
//}===========================================================================

#include "proto.h"

int main()
{
txCreateWindow (1024, 768);

Ball_t ball = {0, 0, 0, 0};

TX_SOCKET ball_server = txCreateSocket (TX_CLIENT, TX_BROADCAST, TX_STD_PORT, TX_BLOCK, false, 1);

const int len = 0;
int sizeofsize = sizeof(len);
        setsockopt (*txGetWinSocket(ball_server), SOL_SOCKET, SO_RCVBUF, (char*) &len, sizeof(len));


if (txnAssert (ball_server) == TXN_NOT_CREATED)
    {
    printf ("Can't create listener. Maybe, port are busy.\n");
    return -1;
    }

while (true)
    {
    if (GetAsyncKeyState ('A'))
        {
        txMessageBox("Meow");

        //The code after this to the next comment is a terrible костыль don`t do like this

/*        int lenold = 0;
        int sizeofsize = sizeof(lenold);
        getsockopt(*txGetWinSocket(ball_server), SOL_SOCKET,
                   SO_RCVBUF, (char *) &lenold, &sizeofsize);

        printf ("RCVBUF size is (%d)\n", lenold);

        const int len = 0;
        sizeofsize = sizeof(len);
        setsockopt (*txGetWinSocket(ball_server), SOL_SOCKET, SO_RCVBUF, (char*) &len, sizeof(len));


        sizeofsize = sizeof(lenold);
        getsockopt(*txGetWinSocket(ball_server), SOL_SOCKET,
                   SO_RCVBUF, (char *) &lenold, &sizeofsize);
        printf ("RCVBUF size is (%d)\n", lenold);

        setsockopt (*txGetWinSocket(ball_server), SOL_SOCKET, SO_RCVBUF, (char*) &lenold, sizeof(lenold));

       */
        }


    txRecvFrom (ball_server, &ball, sizeof(ball));

    if (ball.x == -100 && ball.y == -100)
        break;

    txSetFillColor (TX_LIGHTRED);
    txSetColor (TX_LIGHTRED);

    txCircle (ball.x, ball.y, 10);

    txSleep (25);
    txSetFillColor (TX_BLACK);
    txClear ();
    }

return 0;
}

int txSetSockRecvBufSize (TX_SOCKET& to, int size_, int* oldsize = NULL)
{
int sizeofsize = sizeof(lenold);

int answ = 0;

if (oldsize)
    {
    answ = getsockopt (*txGetWinSocket(ball_server), SOL_SOCKET,
                       SO_RCVBUF, (char *) &oldsize, &sizeofsize);
    if ()

    }


const int len = 0;
int sizeofsize = sizeof(len);
setsockopt (*txGetWinSocket(to), SOL_SOCKET, SO_RCVBUF, (char*) &len, sizeof(len));

}
