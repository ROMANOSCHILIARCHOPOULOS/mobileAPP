const express = require('express');
const bodyParser = require('body-parser');

const app = express();
const PORT = 3000;

let messages = [];

app.use(bodyParser.json());

app.get('/messages', (req, res) => {
    res.json(messages);
});

app.post('/messages', (req, res) => {
    const { message } = req.body;
    messages.push(message);
    console.log('New message:', message);
    res.sendStatus(200);
});

app.listen(PORT, () => {
    console.log(`Server is running on http://localhost:${PORT}`);
});
