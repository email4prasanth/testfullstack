1. Create SG with inbound rules port 3000, 10000, 22 and outbound as allow_all.
2. Edit **E:\Learning\Cloud\DEL_LATER\test-fullstack\server\index.js** as follows
```
app.listen(port, '0.0.0.0', () => {
    console.log(`The server is running on ${port}`);
});

```
3. Access the Backend from the Frontend **E:\Learning\Cloud\DEL_LATER\test-fullstack\client\package.json** add public IPv4 address of your EC2 instanceas as follows 
```
"proxy": "http://44.220.80.249:10000",
```
4. open client session
```
sudo apt install npm -y
npm install react-scripts@latest
npm run build
npm run start
```
4. open server session
```
npm i express nodemon body-parser axios cors dotenv
touch .env
nano .env
npm run start
```