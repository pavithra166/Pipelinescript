pipeline
{
agent none
stages
{
stage('Non-Parallel stage')
{
agent
{
label "master"
}
steps
{
echo 'This stage will be excuted first'
}
}
stage('Run Tests')
{
parallel
{
stage('Test On Windows')
{
agent
{
label "Windows_Node"
}
steps
{
echo "Task1 on Agent"
}
}
stage('Test On Master')
{
agent
{
label "master"
}
steps
{
echo "Task1 on master"
}
}
}
}
}
  

