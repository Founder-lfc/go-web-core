###

测试用例：
```
import (
	"fmt"
	"testing"
	
	"github.com/Founder-lfc/go-web-core/config"
	"github.com/Founder-lfc/go-web-core/config/source/file"
)

func TestApp(t *testing.T)  {
	c, err := config.NewConfig()
	if err != nil {
		t.Error(err)
	}
	err = c.Load(file.NewSource(file.WithPath("config/settings.yml")))
	if err != nil {
		t.Error(err)
	}
	fmt.Println(c.Map())
}
```
