/* Constant declarations */
#DEFINE SOUTH = 0;
#DEFINE NORTH =1;
#DEFINE K = 5;
/*Variable declarations*/
int ER=EW=WR=WW=0;
Semaphore Mutex = 1;
Semaphore South = North =0;
int M = South;
void north2South()
{
wait(Mutex);
/*no active North-bound or no cars*/
if((EW==0 && MM == SOUTH) || (ER+EW+WR+WW == 0){
M=SOUTH;
ER++;
signal(Mutex);
}
else{
WR++:
signal(Mutex);
wait(South);
}
DriveSouthThruTunnel();
wait(Mutex);
ER--;
if(ER == 0 && WW>0){
M=NORTH;
WW--;
EW--;
signal(South);}
signal(Mutex);
}
6
void south2North(){
wait(Mutex);
\\Only no cars
if(ER+EW+WR+WW==0)
{ M=NORTH;
EW++;
signal(Mutex);
}else{
WW++;
//Change if reach K
if(WW==K && MM==SOUTH){
M=NORTH}
signal(Mutex);
wait(North);
}//end of else.
TravelNorthThruTunnel();
wait(Mutex);
EW--;
if(WW>0){
//wake a North bound car
while(WR>0){
WR--;
ER++;
signal(North);
} else {
M=SOUTH;
//Wake up all south cars
while(WR>0) {
WR--;
ER++;
signal(South);
}
}
