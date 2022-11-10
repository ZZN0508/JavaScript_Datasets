var LocalStorageClient = function () {};

LocalStorageClient.prototype.onConnect = function () {
    return new Promise(function (resolve, relect) {
        if (typeof localStorage !== 'undefined' && 'localStorage' in window && window['localStorage'] !== null) {
            resolve('localStorage connected');
        } else {
            reject('localStorage undefined');
        }
    });
}

LocalStorageClient.prototype.set = function (key, data) {
    return new Promise(function (resolve, reject) {
        resolve(localStorage.setItem(key, data));
    });
};

LocalStorageClient.prototype.get = function (key) {
    return new Promise(function (resolve, reject) {
        resolve(localStorage.getItem(key));
    });
};

LocalStorageClient.prototype.del = function (key) {
    return new Promise(function (resolve, reject) {
        resolve(localStorage.removeItem(key));
    });
};

LocalStorageClient.prototype.getKeys = function () {
    return new Promise(function (resolve, reject) {
        var keys = [];
        for (var i = 0;i < localStorage.length;i++) {
            keys.push(localStorage.key(i));
        }
        resolve(keys);
    });
};

LocalStorageClient.prototype.clear = function () {
    return new Promise(function (resolve, reject) {
        resolve(localStorage.clear())
    });
}

LocalStorageClient.prototype.close = function () {
    return new Promise(function (resolve, reject) {
        resolve(true);
    });
};