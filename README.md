# git-commands

#Create repo lên trang git tạo
    --> lệnh đang cập nhật

# Lấy git về từ repo
    --> git clone url_repo

# List nhánh
    --> git branch

# Tạo nhánh 
    --> git branch {ten_nhanh}

# Thoát nhánh
    --> git checkout {branch}

# chuyển nhánh
    --> git switch {branch}

# xoa nhanh
    --> git branch -d {ten_nhanh}

# add file
    --> git add .

# comment 
    --> git command -s "{ noi dung }"


# đây lên theo nhanh

    --> git push origin {ten_nhanh}

# các lệnh khác
    --> git remote add origin https://github.com/username/new_repo

---> postgres set seq

SELECT MAX(id) FROM goose_db_version

SELECT nextval('goose_db_version_id_seq');

SELECT setval('goose_db_version_id_seq', (SELECT MAX(id) FROM goose_db_version));


func ReadJsonGetmessages() ([]model.Message, error) {

	jsonFile, err := os.Open("./jsons/shopee-message.json")
	if err != nil {
		return nil, err
	}

	defer jsonFile.Close()

	byteValue, _ := ioutil.ReadAll(jsonFile)

	var result response.GetMessagesResponse

	er := json.Unmarshal([]byte(byteValue), &result)
	if er != nil {
		return nil, err
	}

	return result.Response.Messages, nil

}

